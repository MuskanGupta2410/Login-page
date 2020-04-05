<template>
  <div class="team">
    <h1 class="subheading grey--text">Team</h1>

    <v-container class="my-5">

      <v-layout row wrap>
        <v-flex xs12 sm6 md4 lg4 v-for="person in team" :key="person.name">
          <v-card flat class="text-xs-center ma-3 d-inline-block" :color="person.color">
            <v-responsive class="pt-4">
              <v-avatar size="100" class="grey lighten-2">
                <img :src="person.character">
              </v-avatar>
            </v-responsive>
            <v-card-text>
              <div class="font-weight-black">{{ person.name }}</div>
              <div class="font-weight-medium">{{ person.role }}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn flat color="grey" align-center>
                <v-icon small left>message</v-icon>
                <span class="">Message</span>
              </v-btn>
              <v-btn icon>
                <v-icon>mdi-share-variant</v-icon>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>

    </v-container>
    
  </div>
</template>


<script>
export default {
 props:{
   source: String
 },
 data() {
    return {
      team: [
        { role: 'Ron Weasley', name: 'Rupert Grint', character: '/character-1.jpg',color: '#E57373'},
        { role: 'Hermoine Granger', name: 'Emma Watson', character: '/character-2.jpg' ,color:'#F06292'},
        { role: 'Harry Potter', name: 'Daniel Radcliffe', character: '/character-3.jpg',color: '#BA68C8'},
        { role: 'Draco Malfoy', name: 'Tom Felton', character: '/character-4.jfif',color:'#26C6DA' },
        { role: 'Rubeus Hagrid', name: 'Robbie Coltrane', character: '/character-5.jfif',color:'#D4E157'},
        { role: 'Albus Dumbledore', name: 'Richard Harris', character: '/character-6.jpg',color:'#FFCA28'},

      ]
    }
  }
}
</script>