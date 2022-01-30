<template>
  <div class="flex flex-col justify-center items-center">
    <h1 class="uppercase text-2xl font-semibold">Generate qrcode</h1>
    <form @submit="qr" class="w-3/4 flex flex-col justify-center items-center" action="/">
      <input class="w-1/2" name="text" type="text" id="text" v-model="text" placeholder="Text...">
      <button class="green-button" type="submit">Generate qrcode</button>
      <div v-if="error" class="mt-4 text-center">
        {{error}}
      </div>
      <div class="mt-4 text-center">
        <h3 class="text-xl">Result:</h3>
        <img :src="img" alt="">
      </div>
    </form>
  </div>
</template>

<script>
import QRCode from 'qrcode'

export default {
  name: 'IndexPage',
  data: () => {
    return{
      text: null,
      img: null,
      error: null
    }
  },
  methods: {
    qr: function (e)  {
      e.preventDefault();
      this.error = null;
      QRCode.toDataURL(this.text)
        .then((url) => {
          this.img = url;
        })
        .catch((err) => {
          this.error = err;
        })
    }
  }
}
</script>
