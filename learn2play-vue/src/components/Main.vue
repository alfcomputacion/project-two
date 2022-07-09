<template>
    <div class="container">
        <Header />
        <SelectInput label="Operations"  value="operation" :options="operations" />
        <SelectInput label="MaxNumber" value="maxNumber" :options="numbers" />
    </div>
</template>

<script>
import Header from './Header.vue'
import SelectInput from './SelectInput.vue'

    export default{
        name: 'Main',
        components: {
    Header,
    SelectInput,
},
    data: function(){
        return{
            operations: [
                ['Addition', '+'],
                ['Subtraction', '-'],
                ['Multiplication', '+'],
                ['Division', '/'],
            ],
            operation: 'x',
            maxNumber: '10'
        }
    },
    methods: {
        play(){
            //do somthing
        }
    },
    computed: {
        numbers: function(){
            const numbers = [];
            for(let number = 2; number < 100; number++){
                numbers.push([number, number]);
            }
            return numbers;
        }
    }

    }
</script>