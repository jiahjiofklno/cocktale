<template>
  <v-app class="bg-blue-lighten-4">
    <section class="pb-10">
      <div>
        <div>
          <v-app-bar
            image="https://img.freepik.com/free-photo/fresh-cocktails-with-ice-lemon-lime-fruits-generative-ai_188544-12370.jpg">
            <v-app-bar-title class="text-white">
              Let's Drink Cocktails..$
            </v-app-bar-title>
            <div class="text-white">
              <v-btn>
                Home
              </v-btn>
              <v-btn>
                About
              </v-btn>
            </div>

          </v-app-bar>
        </div>
      </div>
    </section>


    <section class="py-10">
      <div>
        <div>
          <v-row class="align-center bg-blue-lighten-4">
            <v-col cols="4">
              <v-img width="500px"
                src="https://cheers.com.np/uploads/products/141165677368397147790382205605203059698547.png">

              </v-img>

            </v-col>
            <v-col cols="8">
              <h1 class="text-h3">Drink it and make your Mind fresh....*//</h1>
              <p class="text-h5">
                The self-proclaimed “The strongest beer of Nepal” has lived up to its remarks. It is perfect for all
                occasions, including family reunions, concerts, and dinner parties. It tastes well when combined with
                light meals like salads and hot Nepalese cuisine.Wild Water Buffalo (Bubalus arnee), known as Arna in
                Nepali belongs to family Bovidae of order Aritodactyla. Globally this species is native to Bhutan,
                Cambodia, India, Myanmar, Thailand and Nepal.Arna is a Hindu Girl name, and Arna name meaning is
                Mountain of Strength; Goddess Lakshmi / Durga. It is an Hindi-originated name and the associated lucky
                number is 7. Arna is a short name with 4 letters.</p>
            </v-col>
          </v-row>

        </div>
      </div>
    </section>


    <section>
      <div>
        <div>
          <v-row>
            <v-col cols="3" v-for=" cocktail in products.drinks" :key="cocktail">
              <v-card hover >
                <v-img :src="cocktail.strDrinkThumb":lazy-src="cocktail.strDrinkThumb">
                  
                </v-img>
                <v-card-title> {{ cocktail.strDrink}} </v-card-title>
              </v-card>
            </v-col>
          </v-row>
        </div>
      </div>
    </section>

  </v-app>

</template>

<script setup>
const { data: products } = useFetch("https://www.thecocktaildb.com/api/json/v1/1/filter.php?c=Cocktail")

</script>

<style lang="scss" scoped></style>