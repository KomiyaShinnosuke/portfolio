<template lang="pug">
  #app
    header.header
      .header_inner
        h1.header_title
          router-link(to="/").header_title-link komi's portfolio
        hnav
    main.main
      transition(name="fade")
        router-view(:data="myData")
    footer.footer
      fnav
      .footer_copyright © 2017-2019 komi
</template>

<script>
  import HeaderNav from '@/components/parts/NavHeader'
  import FooterNav from '@/components/parts/NavFooter'
  import myData from '../static/data.json'
  export default {
    name: 'app',
    components: {
      hnav: HeaderNav,
      fnav: FooterNav
    },
    data () {
      return {
        myData: myData
      }
    }
  }
</script>
