<template>
    <div>
        {{$store.state.num}}--
        <!-- {{count}}-- -->
        {{num}}
        <!-- <button @click="$store.commit('add')">+1</button> -->
        <button @click="add()">+1</button>
        <button @click="reduce()">-1</button>
        <!-- <button @click="$store.commit('reduce')">-1</button> -->
    </div>
</template>

<script>
    import store from '@/vuex/store';
    import {mapState,mapMutations} from 'vuex'
    export default {
        store,
        /* computed:{
            count(){
                return this.$store.state.num;
            }
        } */
        /* computed:mapState({
            count(state){
                return state.num;
            }
        }) */
        computed:mapState(['num']),
        methods:mapMutations(['add',reduce])

        
        
    }
</script>

<style scoped>

</style>