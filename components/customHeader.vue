<template>
  <nav
    v-if="header"
    id="mainNav"
    class="navbar navbar-default navbar-fixed-top navbar-custom"
  >
    <div class="container">
      <!-- Brand and toggle get grouped for better mobile display -->
      <div class="navbar-header page-scroll">
        <button
          type="button"
          class="navbar-toggle"
          data-toggle="collapse"
          data-target="#bs-example-navbar-collapse-1"
        >
          <span class="sr-only">Toggle navigation</span> Menu
          <i class="fa fa-bars"></i>
        </button>
        <a class="navbar-brand" href="#page-top">{{ header.title }}</a>
      </div>

      <!-- Collect the nav links, forms, and other content for toggling -->
      <div id="bs-example-navbar-collapse-1" class="collapse navbar-collapse">
        <ul class="nav navbar-nav navbar-left">
          <li class="hidden">
            <a href="#page-top"></a>
          </li>
          
            <li v-for="head in header.logo" :key="head.logo" class="page-scroll">
             <img
                :src="head.logo"
                class="img-responsive"
                :alt="head.logo"
              />
          </li>
          <li v-for="head in header.menu" :key="head.title" class="page-scroll">
            <a :href="'/'">{{ head.title }}</a>
          </li>
          </ul>
        <ul class="nav navbar-nav navbar-right">
          <li class="hidden">
            <a href="#page-top"></a>
          </li>
          
          <li v-for="head in header.details" :key="head.title" >
            <a :href="'/'">{{ head.title }}</a>
          </li>
           
        </ul>
        <ul class="nav navbar-nav navbar-right">
          <!-- <li v-for="head in header.search" :key="head.search" class="page-scroll"> -->
           <input type="text" v-model="search" placeholder="Search title.."/>
          <!-- </li>  -->
          
          </ul>
      </div>
      <!-- /.navbar-collapse -->
    </div>
    <!-- /.container-fluid -->
  </nav>
</template>

<script>
export default {
  props: ["header"],
};
</script>

<style></style>
