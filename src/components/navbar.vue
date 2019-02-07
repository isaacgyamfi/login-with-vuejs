<template>
    <div>
        <b-navbar toggleable="md" type="dark" variant="info">
        <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>

        <b-navbar-brand href="#">Todo App</b-navbar-brand>

        <b-collapse is-nav id="nav_collapse">

            <b-navbar-nav>
            <b-nav-item router-link to="/">Home</b-nav-item>
            <b-nav-item router-link to="/about">About</b-nav-item>
            </b-navbar-nav>

        </b-collapse>
        </b-navbar>

    </div>
</template>

<script>
export default {
    name: 'navbar'
    
}
</script>

<style scoped>

</style>
