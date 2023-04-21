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
            >
                <template #graphic>
                    Graphic
                </template>

                <template #action>
                    Action
                </template>

            </Resume>
        </template>
        <template #movements>
            <Movements
                :movements="movements"
            />
        </template>
    </Layout>
</template>
<script>
import Layout from "./Layout.vue";
import Header from "./Header.vue";
import Resume from "./Resume/Index.vue";
import Movements from "./Movements/Index.vue";

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
            label: null,
            movements: [{
                id: 0,
                title: "Movimiento 1",
                description: "Lorem ipsum dolor sit amet",
                amount: 1000
            },{
                id: 1,
                title: "Movimiento 2",
                description: "Lorem ipsum dolor sit amet",
                amount: 1000
            },{
                id: 2,
                title: "Movimiento 3",
                description: "Lorem ipsum dolor sit amet",
                amount: 1000
            },{
                id: 3,
                title: "Movimiento 4",
                description: "Lorem ipsum dolor sit amet",
                amount: 1000
            },{
                id: 4,
                title: "Movimiento 5",
                description: "Lorem ipsum dolor sit amet",
                amount: 1000
            }]
        }
    }
}

</script>