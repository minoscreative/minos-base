<template>
  <section class="container">
    <div>
      <img src="../assets/images/logo.svg" alt="Minos Creative logo" class="logo" />
      <h1 class="title">
         Welcome
      </h1>
      <h2 class="subtitle">
         Minos Creative website template
      </h2>
    </div>
  </section>
</template>

<script>
   import socialImage from '~/assets/images/logo.svg' //CHANGE TO PAGE IMAGE 800 x 600

   export default {
      head() {
         return {
            title: this.metaData.title,
            meta: [
               { hid: 'description', name: 'description', content: this.metaData.desc },
               { hid: 'og:title', name: 'og:title', content: this.metaData.title },
               { hid: 'og:description', name: 'og:description', content: this.metaData.desc },
               { hid: 'og:url', name: 'og:url', content: this.metaData.url },
               { hid: 'og:image', name: 'og:image', content: process.env.websiteUrl + socialImage }
            ],
            link: [
               { rel: 'canonical', href: this.metaData.url }
            ]
         }
      },
      data() {
         return {
            metaData: {
               title: 'WEBSITE TITLE - Minos Creative',
               desc: '',
               url: process.env.websiteUrl + '/page-url'
            }
         }
      }
   }
</script>

<style>
.container
{
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.title
{
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
.subtitle
{
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  padding-bottom: 15px;
}
.logo {
   width: 20vw;
}

</style>
