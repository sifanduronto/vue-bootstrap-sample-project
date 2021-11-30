<template><div>
  <b-navbar toggleable="lg" style="background-color:white">
    <b-navbar-brand variant="light" href="#"> <b-icon-bar-chart-steps />  <b>Home </b></b-navbar-brand>
    <b-navbar-toggle target="nav-collapse">  
     <b-icon-bar-chart-line-fill /> 
     </b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
         </b-navbar-nav>
      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</div>
</template>
<script>
import { BIconBarChartLineFill,BIconBarChartSteps } from 'bootstrap-vue'

export default{
 components:{
  BIconBarChartLineFill ,
  BIconBarChartSteps
 } ,
 name: 'NavBar',
}
</script>