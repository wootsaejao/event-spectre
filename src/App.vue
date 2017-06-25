<template>
<div id="app">
    <router-view></router-view>
</div>
</template>

<script>
export default {
    name: 'app',
    components: {
    }
}
</script>

<style lang="scss">
@import '~normalize.css';
@import '~font-awesome/css/font-awesome.css';

$primary: #FD0000;
$size-6: 17px;
@import "~bulma";

.container {
    max-width: 700px;
}
</style>
