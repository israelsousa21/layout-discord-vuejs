<template>
  <div class="serverbutton" 
  :class="{'serverbutton-isHome' : isHome, 'serverbutton-hasNotification' : hasNotification}"
  >
  <img src="../../assets/discord.svg" v-if="isHome" />
  <div class="mentions">4</div>
  </div>
</template>
<script>
export default {
    props: {
        selected: Boolean,
        isHome: Boolean,
        hasNotification: Boolean,
        mentions: Number
    }
}
</script>
<style scoped lang="scss">
    .serverbutton{
        margin-top: 8px;
        display: flex;
        flex-shrink: 0;
        align-items: center;
        justify-content: center;
        width: 48px;
        height: 48px;
        background-color: var(--primary);
        cursor: pointer;
        position: relative;
        border-radius: 50%;

        transition: 0.2s;

        &.active,
        &:hover {
            border-radius: 16px;
            background-color: var(--discord);
        }

        img {
            width: 24px;
            height:24px;
        }

        .mentions{
            background-color: var(--notification);
            width:auto;
            height: 24px;
            padding: 0 4px;
            position: absolute;
            border-radius: 12px;
            border: solid 4px var(--quaternary);
            bottom: -4px;
            right: -4px;
            text-align: right;
            font-size: 13px;
            font-weight: bold;
            color: var(--white);
        }
    }

    .serverbutton-isHome {
        background-color: var(--rocketseat);
        &.active,
        &:hover{
            border-radius: 16px;
            background-color: var(--rocketseat);
        }
    }

    .serverbutton-hasNotification{
        &:before{
            content: "";
            width: 9px;
            height: 9px;
            background-color: var(--white);
            position:absolute;
            left:-17px;
            top: calc(50% - 4.5px);
            border-radius: 50%;
            display: block;
        }
    }

    
</style>