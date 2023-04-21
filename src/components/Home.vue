<template>
    <Layout>
        <template #header>
            <Header/>
        </template>
        <template #resume>
            <Resume
                :label="label"
                :labelTotal="'Ahorro total'"
                :totalAmount="1000000"
                :amount="amount"
            />
        </template>
        <template #movements>
            <Movements/>
        </template>
    </Layout>
</template>
<script>
import Layout from "./Layout.vue";
import Header from "./Header.vue";
import Resume from "./Resume/Index.vue";
import Movements from "./Movements.vue";

export default{
    components:{
        Header,
        Layout,
        Resume,
        Movements
    },
    data(){
        return {
            amount: null,
            label: null
        }
    }
}

</script>