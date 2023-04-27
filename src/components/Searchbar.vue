<template>
  <div class="flex items-center bg-white box-border h-18 w-[90%] rounded-lg font-semibold text-gray-600">
    <div class="flex basis-1/6 border-r-2  text-start pl-8" @click="onShowCatClick">
        <img alt="search pic" :src="require('@/assets/images/search.png')" class="h-6 relative top-2.5 right-3">
        <div><p>Category</p><p class="text-gray-400 font-medium">Search...</p></div>
    </div>
    <div class="flex basis-1/6 border-r-2 text-start pl-8">
        <img alt="location pic" :src="require('@/assets/images/location.png')" class="h-5 relative top-2.5 right-3">
        <div><p>Location</p><p class="text-gray-400 font-medium">Select Location</p></div>
    </div>
    <div class="flex basis-1/6 text-start pl-8">
        <img alt="calendar pic" :src="require('@/assets/images/calendar.png')" class="h-5 relative top-2.5 right-3">
        <div><p>Start Date</p>  <input type="date"/></div>
    </div>
    <div class="flex basis-1/6 text-start pl-8">
        <p class="relative top-0 right-4 font-extralight text-4xl text-black">-</p>
        <div><p>End Date</p>    <input type="date"/></div>
    </div>
    <div class="flex basis-1/6 border-l-2 text-start pl-8">
        <img alt="delivery pic" :src="require('@/assets/images/delivery.png')" class="h-7 relative top-2 right-3">
        <div><p>Delivery Method</p><p class="font-medium">Two-way Delivery</p></div>
    </div>
    <div class="basis-1/6 text-center">
        <div class="bg-[#ff3d00] text-white m-5 h-10 flex items-center justify-center rounded-md">Let's Rent</div>
    </div>
  </div>

<!--<a href="https://www.flaticon.com/free-icons/magnifying-glass" title="magnifying glass icons">Magnifying glass icons created by Ayub Irawan - Flaticon</a>-->
<!--<a href="https://www.flaticon.com/free-icons/location" title="location icons">Location icons created by Yogi Aprelliyanto - Flaticon</a>-->
<!--<a href="https://www.flaticon.com/free-icons/calendar" title="calendar icons">Calendar icons created by bqlqn - Flaticon</a>-->
<!--<a href="https://www.flaticon.com/free-icons/delivery" title="delivery icons">Delivery icons created by Kiranshastry - Flaticon</a>-->
</template>

<script>
export default {
    data() {
        return {

        }
    },
    methods: {
        onShowCatClick() {
            this.$emit('showCatClicked')
            console.log('clicked')
        }
    }
}
</script>

<style>

</style>