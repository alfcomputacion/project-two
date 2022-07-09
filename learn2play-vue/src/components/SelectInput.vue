<template>
    <div class="container">
        <label :for="id">{{label}}</label>
        <select :id="id">
            <option 
                v-for="option in options" 
                :key="option[1]" 
                :value="option[1]">
                {{option[0]}}
            </option>
        </select>
    </div>
</template>

<script>
    export default{
        name: 'SelectInput',
        props: {
            label: String,
            id: String,
            options: Array,
            currentValue: String,
            maxNumber: String
        }
    }
</script>