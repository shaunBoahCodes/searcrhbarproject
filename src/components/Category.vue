<template>

<div class="bg-white h-[67vh] w-[90%] mt-1 rounded-lg" id="Modal">
  <div id="grid-container" class="h-[100%] rounded-lg grid grid-cols-[1fr_2fr] grid-rows-[60px_auto] text-[17px] font-medium">
      <div id="search-bar" class="item col-span-2 flex items-center pl-10 border-b-[2px] border-gray-100">
          <img alt="search pic" :src="require('@/assets/images/search.png')" class="h-6 relative right-3">
          <input type="text" placeholder="What are you looking for?" class="w-[90%]"/>
      </div>
      <div id="contents" class="overflow-scroll rounded-bl-lg">
          <div v-for="category in categories" :key="category" 
                class="h-14 flex items-center pl-7 text-[15px] 
                font-semibold text-gray-500 bg-gray-100 hover:bg-gray-300" @mouseover="updateDescription(category.description)">
                {{ category.name }}</div>
      </div>
      <div id="description" class="item">{{ currentDescription }}</div>
  </div>
</div>

</template>

<script>
export default {
    data() {
        return {
            categories: [ {'name': 'Aerial Working Platform', 'description': '1897'}, 
                          {'name': 'Earth Moving', 'description': '8391'}
                          //, 'Material Handling', 'Compaction Equipment', 
                        //'Lifting Equipment', 'Vehicle', 'Site Preparation & Services', 'Light Equipment & Tools'
                        ],
            currentDescription: ''
        }
    },
    methods: {
        updateDescription(description) {
            this.currentDescription = description
        }
    }
}
</script>

<style>
#Modal {
  box-shadow: 0 0 20px rgba(0,0,0,0.3);
}
input:focus, textarea:focus, select:focus {
      outline: none;  
}
</style>