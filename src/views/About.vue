<template>
    <NavBar/>
    <h3>This is an About Page</h3>
    <h2>Welcome to CPP</h2>
    <h3>CPP Description: Lorem ipsum dolor sit amet consectetur adipisicing elit. Suscipit eum natus illo ipsam eveniet in ullam, quisquam recusandae tenetur voluptates earum iusto non nulla porro? Perferendis quos dignissimos recusandae veritatis?  </h3>
    <LogOut/> <br><br>
</template>

<script>
import NavBar from '@/components/NavBar.vue'
import LogOut from '@/components/LogOut.vue'

export default {
    
    name:"About",
    components : {
        NavBar,
        LogOut
    }
}
</script>