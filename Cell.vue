<template>
    <button class="cell" @click="$emit('move_cell', id_cell)">
        {{value != 0? value : ""}}
    </button>
</template>

<script>
    export default {
        name: 'Cell',
        props: {
            id_cell: Number,
            value: {
                type: Number,
                default: 0
            }
        }
    }
</script>
<style scoped lang="scss">
    .cell {
        outline: none;
        width: 100px;
        height: 100px;
        position: relative;
        border: 1px solid #8ed3c9;
        background: #8ed3c9;
        color: white;
        border-radius: 10px;
        text-align:center;
        font-size: 40px;
        font-family: "Segoe UI";
        cursor: default;
        justify-content: center;
        transition: all .5s linear;

    }
    .cell:hover {
        box-shadow: 0 0 10px rebeccapurple;
        opacity: 0.5;
    }

</style>
