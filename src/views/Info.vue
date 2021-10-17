<template>
  <v-container 
    class="text-center"
    v-if="this.$route.params.savedForm"
  >
    <div class="header">
        <div class="header-content">
            <div class="col-4 primary d-inline-block rounded-tl-lg"></div>
            <div class="col-4 secondary d-inline-block"></div>
            <div class="col-4 accent d-inline-block rounded-tr-lg"></div>
        </div>
    </div>
    <v-card
      class="mx-auto px-7 py-10 rounded-b-lg rounded-t-0"
      max-width="800"
      outlined
      elevation="3"
    >
      <h1 class="text-headline success--text">
        Berhasil!
      </h1>

      <v-divider class="my-2"></v-divider>

      <p>
        Data berhasil disimpan.
      </p>
      <v-btn
        rounded
        color="success"
        class="rounded-pill px-16 py-6"
        to="/"
      >
        Tambah Data Baru
      </v-btn>
    </v-card>
  </v-container>
</template>

<script>
  export default {
    data: () => ({
      
    }),
    beforeCreate(){
      if(!this.$route.params.savedForm){
        console.log("masuk")
        this.$router.push("/");
      }

    },   
    mounted(){
    }
  }
</script>