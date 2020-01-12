<template>
  <v-container class="main">
    <div>
      <h1 class="text-purple">
        Meus certificados
      </h1>
    </div>
    <div class="cards-box">
      <div class="image-background">
        <img src="../assets/medalha-image.svg" alt="Imagem medalhas">
      </div>
      <div class="footer">
        <div class="title-socias">
          <strong class="title-black">Matemática na prática</strong>
          <!-- <div class="icon-share">
          <img src="../assets/facebook.png" alt="">
              <img src="../assets/google.png" alt="">
              <img src="../assets/instagram.png" alt="">
            </div>
            <button type="button" class="comp" @click="share">
              <img class="compartilhe" src="../assets/icon-social-shape_24px.svg" alt="">
            </button>
          </div> -->
          <div class="icon-share">
            <shareBtn />
          </div>
        </div>
        <p>Thiago Carvalho</p>
        <div class="cards-box">
          <div class="image-background">
            <img src="../assets/medalha-image.svg" alt="Imagem medalhas">
          </div>
          <div class="footer">
            <div class="title-socias">
              <strong class="title-black">Matemática na prática</strong>
              <!-- <div class="icon-share">
              <img src="../assets/facebook.png" alt="">
              <img src="../assets/google.png" alt="">
              <img src="../assets/instagram.png" alt="">
            </div>
            <button type="button" class="comp" @click="share">
              <img class="compartilhe" src="../assets/icon-social-shape_24px.svg" alt="">
            </button> -->
            </div>
            <p>Thiago Carvalho</p>
          </div>
        </div>
      </div>
    </div>
  </v-container>
</template>
<script>
import shareBtn from '../components/shareBtn'

export default {
  components: {
    shareBtn
  }
  // data: () => ({
  //   certifactes: []
  // }),
  // mounted () {
  //   certificateService.findAllCertificatesByUser('48310300-e9d2-4d9c-929e-ed626126673e')
  //     .then((certificates) => {
  //       this.certificates = certificates.data
  //       console.log(certificates)
  //     }).catch(error => console.log(error))
  // },
  // methods: {
  //   backgroundClass (certificateBackgroundName) {
  //     return `background-image: url(/_nuxt/assets/${certificateBackgroundName})`
  //   },
  //   share () {
  //     alert('Try-out')
  //   }
  // }
}
</script>
<style>
  .main {
    margin-top: 30px;
    width: 375px;
  }

  * {
    margin: 0;
    padding: 0;
  }

  button {
    /* display: none; */
    cursor: pointer !important;
  }

  .cards-box {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .card {
    margin-top: 10px;
  }
  .text-purple {
    font-family: Montserrat;
    color: #6600CC;
    font-size: 16px;
    text-transform: uppercase;
    padding-left: 34px;
    margin-bottom: 10px;
  }
  .image-background {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 200px;
    height: 115px;
    background: #6600cc url("../assets/matematica.svg");
    /* background: #6600cc url("../assets/fotografia.svg");
    background: #6600cc url("../assets/cenografia.svg") */
  }

  .footer {
    width: 200px;
    padding-top: 10px;
    line-height: 15px;
    text-align: center;

    font-family: Montserrat;
    font-style: normal;
    font-weight: 500;
  }
  .title-black {
    font-family: Montserrat;
    font-style: normal;
    font-weight: 600;
    font-size: 12px;
    line-height: 15px;
    display: flex;
    color: #1A1A1A;
    padding-left: 2px;

    align-items: center;
    text-align: center;

  }

  .footer p {
    font-family: Montserrat;
    font-style: normal;
    font-weight: 300;
    font-size: 10px;
    line-height: 12px;
    padding-left: 2px;

    color: #1A1A1A;
    margin-top: 10px;
    display: flex;
    align-items: center;

  }
  .title-socias {
    font-family: Montserrat;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .compartilhe {
    max-width: 24px;
  }

  .icon-share{
    position: absolute;
    margin: 0 0 0 110px
    /* display: flex;
    align-items: center;
    justify-content: space-around; */

    /* display: none;
    width: 90px;
    height: 35px; */
    /* background: #6600CC; */
    /* box-shadow: 2px 4px 4px rgba(0, 0, 0, 0.25); */
  }
</style>
