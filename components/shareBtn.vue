<template>
  <v-layout>
    <div v-if="isOpen" class="share-container">
      <social-sharing
        :url="url"
        :title="title"
        :description="description"
        :hashtags="hashtags"
        :twitter-user="twitterUser"
        @open="isOpen = !isOpen"
        inline-template
      >
        <div class="icons">
          <network network="facebook">
            <v-icon color="#fff" size="30">
              mdi-facebook
            </v-icon>
          </network>
          <network network="twitter">
            <v-icon color="#fff" size="30">
              mdi-twitter
            </v-icon>
          </network>
          <network network="linkedin">
            <v-icon color="#fff" size="30">
              mdi-linkedin
            </v-icon>
          </network>
        </div>
      </social-sharing>
    </div>
    <v-btn
      v-if="!isOpen"
      :color="color"
      @click="isOpen = !isOpen"
      class="ma-2"
      tile
      large
      icon
    >
      <v-icon>
        mdi-share-variant
      </v-icon>
    </v-btn>
  </v-layout>
</template>

<script>
import SocialSharing from 'vue-social-sharing'

export default {
  components: {
    SocialSharing
  },

  props: {
    color: {
      default: '#CCC'
    },
    url: String,
    title: String,
    description: String,
    hashtags: {
      default: 'MissaoNewSchoolApp'
    },
    twitterUser: {
      default: 'NewSchoolApp'
    }
  },

  data () {
    return {
      isOpen: false
    }
  }
}
</script>

<style>
.share-container {
  width: 90px;
  height: 35px;
  background: #60C;
}

.icons {
  display: flex;
}

.share-container .icons network v-icons {
  max-width: 5px;
}

.facebook {
  max-width: 5px;
}

.ma-2 {
  padding-left: 55px;
}
</style>
