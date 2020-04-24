<template>
  <div class="Product">
    <HeaderShayna />
    <!-- Breadcrumb Section Begin -->
    <div class="breacrumb-section">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="breadcrumb-text product-more text-left">
              <router-link to="/">
                <i class="fa fa-home"></i> Home
              </router-link>
              <span>Detail</span>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Breadcrumb Section Begin -->

    <!-- Product Shop Section Begin -->
    <section class="product-shop spad page-details">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="row">
              <div class="col-lg-6">
                <div class="product-pic-zoom">
                  <img class="product-big-img" :src="gambar_default" alt />
                </div>
                <div class="product-thumbs">
                  <carousel class="product-thumbs-track ps-slider" :dots="false" :nav="false">
                    <div
                      class="pt"
                      v-on:click="gantiImage(thumbs[0])"
                      :class="thumbs[0] == gambar_default ? 'active':'' "
                    >
                      <img src="img/sepatu1.jpg" alt />
                    </div>

                    <div
                      class="pt"
                      v-on:click="gantiImage(thumbs[1])"
                      :class="thumbs[1] == gambar_default ? 'active':'' "
                    >
                      <img src="img/sepatu2.jpg" alt />
                    </div>

                    <div
                      class="pt"
                      v-on:click="gantiImage(thumbs[2])"
                      :class="thumbs[2] == gambar_default ? 'active':'' "
                    >
                      <img src="img/sepatu3.jpg" alt />
                    </div>

                    <div
                      class="pt"
                      v-on:click="gantiImage(thumbs[3])"
                      :class="thumbs[3] == gambar_default ? 'active':'' "
                    >
                      <img src="img/kets1.jpg" alt />
                    </div>
                  </carousel>
                </div>
              </div>
              <div class="col-lg-6">
                <div class="product-details text-left">
                  <div class="pd-title">
                    <span>black</span>
                    <h3>Sepatu</h3>
                  </div>
                  <div class="pd-desc">
                    <p>
                      Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis, error
                      officia. Rem aperiam laborum voluptatum vel, pariatur modi hic provident eum
                      iure natus quos non a sequi, id accusantium! Autem.
                    </p>
                    <p>
                      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quam possimus quisquam
                      animi, commodi, nihil voluptate nostrum neque architecto illo officiis
                      doloremque et corrupti cupiditate voluptatibus error illum. Commodi expedita
                      animi nulla aspernatur.
                      Id asperiores blanditiis, omnis repudiandae iste inventore cum, quam sint
                      molestiae accusamus voluptates ex tempora illum sit perspiciatis. Nostrum dolor
                      tenetur amet, illo natus magni veniam quia sit nihil dolores.
                      Commodi ratione distinctio harum voluptatum velit facilis voluptas animi non
                      laudantium, id dolorem atque perferendis enim ducimus? A exercitationem
                      recusandae aliquam quod. Itaque inventore obcaecati, unde quam
                      impedit praesentium veritatis quis beatae ea atque perferendis voluptates velit
                      architecto?
                    </p>
                    <h4>$495.00</h4>
                  </div>
                  <div class="quantity">
                    <router-link to="/ShopingCart" class="primary-btn pd-cart">Add To Cart</router-link>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Product Shop Section End -->

    <relatedProduct />
    <FooterShayna />
  </div>
</template>

<script>
// @ is an alias to /src
import HeaderShayna from "@/components/HeaderShayna.vue";
import FooterShayna from "@/components/FooterShayna.vue";
import relatedProduct from "@/components/relatedProduct.vue";

import carousel from "vue-owl-carousel";

export default {
  name: "Product",
  components: {
    HeaderShayna,
    FooterShayna,
    relatedProduct,
    carousel
  },

  data() {
    return {
      gambar_default: "img/sepatu1.jpg",
      thumbs: [
        "img/sepatu1.jpg",
        "img/sepatu2.jpg",
        "img/sepatu3.jpg",
        "img/kets1.jpg"
      ]
    };
  },
  methods: {
    gantiImage(gambar) {
      this.gambar_default = gambar;
    }
  }
};
</script>

<style scoped>
.product-thumbs .pt {
  margin-right: 14px;
}
</style>
