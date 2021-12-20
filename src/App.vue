<template>
    <div id="app">
        <CKHeader></CKHeader>
        <CKContent></CKContent>

    </div>

</template>

<script>
    import CKHeader from './components/CKHeader.vue'
    import CKContent from './components/CKContent.vue'


export default{
    components: {
        'CKHeader' : CKHeader,
        'CKContent' : CKContent
    }
}
    
</script>

<style>
#app {
    background-color: #171010;
    width: 1903px;
    height: 1200px;
    margin: 0 auto;
    font-family: 'Nanum Gothic', sans-serif;
    z-index: -10;
}
</style>