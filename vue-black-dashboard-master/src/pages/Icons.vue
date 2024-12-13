<template>
  <div class="card">
    <div class="card-header">
      <div class="typography-line">
            <h1><span>Header 1</span>Browse your favourite sport!</h1>
          </div>
      <p class="category">
        Handcrafted by our friends from
        <a href="https://nucleoapp.com/?ref=1712">NucleoApp</a>
      </p>
    </div>
    <div class="card-body all-icons">
      <div class="row">
        <div
    class="font-icon-list col-lg-2 col-md-3 col-sm-4 col-xs-6 col-xs-6"
    v-for="(icon, index) in icons"
    :key="index"

  >
          <div
          :style="{
						backgroundImage: icon.image ? `url(${require(`@/assets/img/${icon.image}`)})` : 'url(/default-image.jpg)',
						backgroundSize: 'cover',
						backgroundPosition: 'center',
						backgroundRepeat: 'no-repeat'
					}"
          class="font-icon-detail">
            <i :class="icon.class"></i>
            <p>{{ icon.label }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      icons: [
        { class: 'tim-icons icon-book-bookmark', label: 'Book Bookmark', image: 'bad.jpg' },
        { class: 'tim-icons icon-bold', label: 'Bold', image: 'circ.png' },
        { class: 'tim-icons icon-italic', label: 'Italic', image: 'cyc.jpg' },
        { class: 'tim-icons icon-pencil', label: 'Pencil', image: 'kabb.jpg' },
      ],
    };
  },
};
</script>

<style scoped>
/* Add your styles here */
</style>
