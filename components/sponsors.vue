<template>
  <div class="sponsors-container">
    <div
      v-for="(sponsor, index ) in sponsors"
      class="sponsor"
      :style="{backgroundImage: 'url(' + sponsor + ')'}"
      :key="index"
    ></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: ["/logo.png"]
    };
  },
  computed: {
    sponsors() {
      let sponsorsArray = [];
      let width = 10000;
      let index = 0;
      let length = this.images.length;
      while (width > 0) {
        if (index >= length) index = 0;
        sponsorsArray.push(this.images[index]);
        width -= 300;
        index++;
      }
      return sponsorsArray;
    }
  }
};
</script>

<style>
.sponsors-container {
  position: absolute;
  width: 10000px;
  bottom: 0;
  display: flex;
  flex-wrap: nowrap;
  animation-name: scroll;
  animation-iteration-count: infinite;
  animation-duration: 15s;
  animation-timing-function: linear;
  background-color: rgba(0, 0, 0, 0.3);
  margin: 0.5rem 0;
}

.sponsor {
  height: 150px;
  width: 150px;
  margin-right: 100px;
  background-size: cover;
  background-position: center;
}

@keyframes scroll {
  from {
    transform: translateX(0);
  }

  to {
    transform: translateX(-50%);
  }
}
</style>

