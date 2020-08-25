<template>
 <div class="container">
   <ServerButton isHome />
   <div class="separator"></div>
   <ServerButton hasNotification :mentions="3"/>
   <ServerButton hasNotification :mentions="11" />
   <ServerButton :mentions="21" hasNotification/>
   <ServerButton v-for="servers in 18" :key="servers.id" />
 </div>   
</template>
<script>
import ServerButton from './ServerButton'
export default {
    components:{
        ServerButton
    }
}   
</script>
<style scoped lang="scss">
.container {
    grid-area: SL;
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: var(--tertinary);
    padding: 11px 0;
    max-height: 100vh;
    overflow: scroll;
    &::-webkit-scrollbar {
        display: none;
    }
    scrollbar-width: none;
}

.separator {
    width: 32px;
    border-bottom: solid 2px var(--quaternary);
    margin-bottom: 8px;
    margin-top: 16px;
}
</style>