<template>
    <NavBar/>
    <h3>This is Profit Page</h3>
    <ProfitDisplay/>
    <LogOut/>
</template>


<script>
import ProfitDisplay from '@/components/ProfitDisplay.vue'
import NavBar from '@/components/NavBar.vue'
import LogOut from '@/components/LogOut.vue'

export default {
    name: 'OnlyProfit',
    components: {
        ProfitDisplay,
        NavBar,
        LogOut
    }
}
</script>