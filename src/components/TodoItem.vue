<script >
export default {
    name: 'TodoItem',
    props: {
        todo: Object
    }
}
</script>

<template lang="">
<li>
    <p>
        {{ todo.text }}
    </p>
</li>
</template>



<style lang="">


    
</style>