<template>
    <div class="product">
  
        <HeaderShayna />

        <!-- Breadcrumb Section Begin -->
        <div class="breacrumb-section text-left">
            <div class="container">
                <div class="row">
                    <div class="col-lg-12">
                        <div class="breadcrumb-text product-more">
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
                                    <img class="product-big-img" :src="pic_default" alt="" />
                                </div>
                                <div class="product-thumbs">

                                    <carousel class="product-thumbs-track ps-slider"
                                    :nav="false" :dots="false">
                                        <div class="pt" @click="changeImage(thumbs[0])" :class=" thumbs[0] == pic_default ? 'active' : '' ">
                                            <img src="img/ootd-1.jpg" alt="" />
                                        </div>

                                        <div class="pt" @click="changeImage(thumbs[1])" :class=" thumbs[1] == pic_default ? 'active' : '' ">
                                            <img src="img/ootd-1a.png" alt="" />
                                        </div>

                                        <div class="pt" @click="changeImage(thumbs[2])" :class=" thumbs[2] == pic_default ? 'active' : '' ">
                                            <img src="img/ootd-1b.png" alt="" />
                                        </div>

                                        <div class="pt" @click="changeImage(thumbs[3])" :class=" thumbs[3] == pic_default ? 'active' : '' ">
                                            <img src="img/ootd-1c.png" alt="" />
                                        </div>

                                        <div class="pt" @click="changeImage(thumbs[4])" :class=" thumbs[4] == pic_default ? 'active' : '' ">
                                            <img src="img/ootd-1d.png" alt="" />
                                        </div>
                                    </carousel>

                                </div>
                            </div>
                            <div class="col-lg-6">
                                <div class="product-details text-left">
                                    <div class="pd-title">
                                        <span>Winter</span>
                                        <h3>Brownie Monday</h3>
                                    </div>
                                    <div class="pd-desc">
                                        <p>
                                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis, error officia. Rem aperiam laborum voluptatum vel, pariatur modi hic provident eum iure natus quos non a sequi, id accusantium! Autem.
                                        </p>
                                        <p>
                                            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quam possimus quisquam animi, commodi, nihil voluptate nostrum neque architecto illo officiis doloremque et corrupti cupiditate voluptatibus error illum. Commodi expedita animi nulla aspernatur.
                                            Id asperiores blanditiis, omnis repudiandae iste inventore cum, quam sint molestiae accusamus voluptates ex tempora illum sit perspiciatis. Nostrum dolor tenetur amet, illo natus magni veniam quia sit nihil dolores.
                                            Commodi ratione distinctio harum voluptatum velit facilis voluptas animi non laudantium, id dolorem atque perferendis enim ducimus? A exercitationem recusandae aliquam quod. Itaque inventore obcaecati, unde quam
                                            impedit praesentium veritatis quis beatae ea atque perferendis voluptates velit architecto?
                                        </p>
                                        <h4>$495.00</h4>
                                    </div>
                                    <div class="quantity">
                                        <router-link to="/cart">
                                            <a href="shopping-cart.html" class="primary-btn pd-cart">Add To Cart</a>
                                        </router-link>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <!-- Product Shop Section End -->

        <RelatedProduct />
        <FooterShayna />
        
  
    </div>
  </template>
  
  <script>
  // @ is an alias to /src
  // import HelloWorld from '@/components/HelloWorld.vue'
  import HeaderShayna from '@/components/HeaderShayna.vue';
  import RelatedProduct from '@/components/RelatedProduct.vue';
  import FooterShayna from '@/components/FooterShayna.vue';
  import carousel from 'vue-owl-carousel';
  
  export default {
    name: 'Product',
    components: {
      HeaderShayna,
      carousel,
      RelatedProduct,
      FooterShayna
    },
    data() {
        return {
            pic_default: "img/ootd-1.jpg",
            thumbs: [
                "img/ootd-1.jpg",
                "img/ootd-1a.png",
                "img/ootd-1b.png",
                "img/ootd-1c.png",
                "img/ootd-1d.png"
            ]
        }
    },
    methods: {
        changeImage(urlImage) {
            this.pic_default = urlImage;
        }
    }
  };
  </script>
  
  <style scoped>
    .product-thumbs .pt {
        margin-right: 5px;
        margin-left: 5px;
    }
    .product-thumbs .pt img {
        max-height: 150px;
    }
  </style>