<template>
 <b-row>
 <b-col offset-lg="3" offset-md="2" lg="6" sm="12" md="8">
<b-list-group>
  <b-list-group-item  v-for="item in items" :key="item.id" variant="white" class="b__list__group__item__text__color d-flex justify-content-between align-items-center">
   {{ item.name}}
    <b-badge variant="light" pill>i</b-badge>
  </b-list-group-item>
 <b-list-group-item  variant="light" class="d-flex justify-content-between align-items-center">
       Item Icon pic  <br>
      <b-btn> Select Image file </b-btn>

     <b-img v-bind="iconIconPicProps" rounded="top" alt="Top-rounded image"></b-img>
 <b-badge variant="light" pill>i</b-badge>
  </b-list-group-item>
  <b-list-group-item  variant="light" class="d-flex justify-content-between align-items-center">
       Item pic  <br>
     <b-btn> Select Image file </b-btn>
     <b-img v-bind="itemPicProps" rounded="top" alt="Top-rounded image"></b-img>
 <b-badge variant="light" pill>i</b-badge>
  </b-list-group-item>
  
</b-list-group>

<a @click="advanceSettings ? advanceSettings = false : advanceSettings = true "> Advance Item settings </a>
<div v-if="advanceSettings">
<Header title="Sizes" />
 <b-list-group-item  variant="light" class="d-flex justify-content-between align-items-center">
 <strong>  Add Size </strong>
    <b-badge variant="light" pill>+</b-badge>
  </b-list-group-item>
<Header title="Addons" />
 <b-list-group-item  variant="light" class="d-flex justify-content-between align-items-center">
 <strong> Add new addons  </strong>
   <b-badge variant="light" pill>+</b-badge> 
  </b-list-group-item>
 <Header title="Customizations" />
 <b-list-group-item  variant="light" class="d-flex justify-content-between align-items-center">
<strong> Add new customizations </strong>
    <b-badge variant="light" pill>+</b-badge>
  </b-list-group-item>
</div>
    </b-col>  
    <b-col cols="12" offset-lg="3" offset-md="3" lg="6" sm="12" md="6">
    <b-button  pill class ="item__form__submission_button mt-2"> <b>SAVE </b> </b-button>
    </b-col>
  </b-row>
</template>
<script>
import Header from './Header.vue'
export default {
  components:{
    Header
  },
  name: 'ItemList',   
  data(){
  return {
    advanceSettings:false,
    itemPicProps: { blank: true, blankColor: '#777', width: 100, height: 100, class: 'm1' },
    iconIconPicProps: { blank: true, blankColor: '#777', width: 75, height: 75, class: 'm1' },
    items:[{
     name: 'Item name',
     id:1,
   },
   {
     name: 'Item English Name',
     id:2,
   },{
     name: 'Price',
     id:3,
   },{
     name: 'Calories',
     id:4,
   }]
  }
  }
}
</script>

