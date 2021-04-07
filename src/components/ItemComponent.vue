<template>
    <div class="box">
        <ul>
            <li>{{element}}</li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'ItemComponent',
    props: {
        element: String
    }
}
</script>

<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
</style>

