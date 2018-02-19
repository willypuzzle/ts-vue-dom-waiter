<template>
<div :id="'waiter-background-' + randString()" v-if="active" style="background-color: #075c90; opacity: 0.8; width: 100%; height: 100%; position: fixed; z-index: 99999998;top: 0; left: 0;">
    <div style="position:fixed; top:50%; left:50%; z-index:99999999;" >
        <div class="sk-cube-grid">
            <div class="sk-cube sk-cube1"></div>
            <div class="sk-cube sk-cube2"></div>
            <div class="sk-cube sk-cube3"></div>
            <div class="sk-cube sk-cube4"></div>
            <div class="sk-cube sk-cube5"></div>
            <div class="sk-cube sk-cube6"></div>
            <div class="sk-cube sk-cube7"></div>
            <div class="sk-cube sk-cube8"></div>
            <div class="sk-cube sk-cube9"></div>
        </div>
    </div>
</div>
</template>
<script>export default {
    props: {
        active: false
    },
    methods: {
        randString: function () {
            return Math.random().toString(36).replace(/[^a-z]+/g, '').substr(0, 5);
        }
    }
};
</script>

<style >
   /*
*  Usage:
*
     <div class="sk-cube-grid">
       <div class="sk-cube sk-cube1"></div>
       <div class="sk-cube sk-cube2"></div>
       <div class="sk-cube sk-cube3"></div>
       <div class="sk-cube sk-cube4"></div>
       <div class="sk-cube sk-cube5"></div>
       <div class="sk-cube sk-cube6"></div>
       <div class="sk-cube sk-cube7"></div>
       <div class="sk-cube sk-cube8"></div>
       <div class="sk-cube sk-cube9"></div>
     </div>
*
*/

   .sk-cube-grid {
       width: 80px;
       height: 80px;
       margin: -40px -40px;
       /*
        * Spinner positions
        * 1 2 3
        * 4 5 6
        * 7 8 9
        */ }
   .sk-cube-grid .sk-cube {
       width: 33.33%;
       height: 33.33%;
       background-color: #ffd530;
       float: left;
       -webkit-animation: sk-cubeGridScaleDelay 1.3s infinite ease-in-out;
       animation: sk-cubeGridScaleDelay 1.3s infinite ease-in-out; }
   .sk-cube-grid .sk-cube1 {
       -webkit-animation-delay: 0.2s;
       animation-delay: 0.2s; }
   .sk-cube-grid .sk-cube2 {
       -webkit-animation-delay: 0.3s;
       animation-delay: 0.3s; }
   .sk-cube-grid .sk-cube3 {
       -webkit-animation-delay: 0.4s;
       animation-delay: 0.4s; }
   .sk-cube-grid .sk-cube4 {
       -webkit-animation-delay: 0.1s;
       animation-delay: 0.1s; }
   .sk-cube-grid .sk-cube5 {
       -webkit-animation-delay: 0.2s;
       animation-delay: 0.2s; }
   .sk-cube-grid .sk-cube6 {
       -webkit-animation-delay: 0.3s;
       animation-delay: 0.3s; }
   .sk-cube-grid .sk-cube7 {
       -webkit-animation-delay: 0.0s;
       animation-delay: 0.0s; }
   .sk-cube-grid .sk-cube8 {
       -webkit-animation-delay: 0.1s;
       animation-delay: 0.1s; }
   .sk-cube-grid .sk-cube9 {
       -webkit-animation-delay: 0.2s;
       animation-delay: 0.2s; }
   @-webkit-keyframes sk-cubeGridScaleDelay {
       0%, 70%, 100% {
           -webkit-transform: scale3D(1, 1, 1);
           transform: scale3D(1, 1, 1); }
       35% {
           -webkit-transform: scale3D(0, 0, 1);
           transform: scale3D(0, 0, 1); } }
   @keyframes sk-cubeGridScaleDelay {
       0%, 70%, 100% {
           -webkit-transform: scale3D(1, 1, 1);
           transform: scale3D(1, 1, 1); }
       35% {
           -webkit-transform: scale3D(0, 0, 1);
           transform: scale3D(0, 0, 1); } }
</style>