<template>
  <div class="container-user-info">
    <div class="profile">
        <div class="avatar">
          <img src="https://github.com/israelsousa21.png" />
        </div>
      
      <div class="userdata">
        <strong>Israel Sousa</strong>
        <span>#2121</span>
      </div>
    </div>
    <div class="actions">
      <MicIcon :size="20" />
      <HeadphoneIcon :size="20" />
      <SettingsIcon :size="20" />
    </div>
  </div>
</template>

<script>
import MicIcon from "vue-material-design-icons/Microphone";
import HeadphoneIcon from "vue-material-design-icons/Headphones";
import SettingsIcon from "vue-material-design-icons/CogOutline";
export default {
  components: {
    MicIcon,
    HeadphoneIcon,
    SettingsIcon,
  },
};
</script>

<style scoped lang="scss">
.container-user-info {
  grid-area: UI;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 10px;
  background-color: var(--quaternary);
  box-shadow: rgba(0, 0, 0, 0.2) 0 1px 0;
  .profile{
      display: flex;
      align-items: center;
  }
  .avatar {
      
      display: flex;
      align-items: center;
      width: 33px;
      height: 33px;
      border-radius: 50%;
      background-color: var(--gray);
      border: solid 1px color(--white);
      img {
          margin-top: 1px;
          width: 32px;
          height: 32px;
          border-radius: 50%;
      }
  }
  .userdata {
      display: flex;
      flex-direction: column;
      margin-left: 8px;
      font-size: 13px;
      
      strong {
          display: block;
          color: var(--white);
      }

      span {
          color: var(--gray);
      }
  }

    .actions {
        color: var(--gray);

        span {
            cursor: pointer;
            transition: 0.2s;
            
            &:hover{
                color: var(--white);
            }
        }
    }

}

</style>