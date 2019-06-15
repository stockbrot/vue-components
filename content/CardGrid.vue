<template>
  <v-layout class="cardcomp" row wrap>
    <v-flex
      v-for="card in cards"
      :key="card.id"
      v-bind="{ [`xs${card.flex}`]: true }"
    >
      <v-card>
        <v-img
          :src="`https://unsplash.it/650/300?image=${Math.floor(Math.random() * 100) + 1}`"
          height="200px"
        >
          <v-container
            fill-height
            fluid
            pa-2
          >
            <v-layout fill-height>
              <v-flex xs12 align-end flexbox>
                <span class="headline white--text" v-text="card.title"></span>
              </v-flex>
            </v-layout>
          </v-container>
        </v-img>

        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn icon>
            <v-icon>favorite</v-icon>
          </v-btn>
          <v-btn icon>
            <v-icon>bookmark</v-icon>
          </v-btn>
          <v-btn icon>
            <v-icon>share</v-icon>
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
  export default {
    name: 'CardGridComp',
    data () {
      return {
        cards: [
          { title: 'Pre-fab homes', flex: 12, id: 0 },
          { title: 'Favorite road trips', flex: 9, id: 1 },
          { title: 'Favorite road trips', flex: 3, id: 2 },
          { title: 'Favorite road trips', flex: 6, id: 3 },
          { title: 'Favorite road trips', flex: 6, id: 4 },
          { title: 'Best airlines', flex: 6, id: 5 }
        ]
      }
    }
  }
</script>

<style lang="stylus">
  .cardcomp
    width 100%
</style>
