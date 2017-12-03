<template>
  <div>
    {/*桌面上的图标*/}
    <div ref="desktopManager" id="desktop" class="desktopIcon-manager">
      <ul id="icons" class="icons">
        {iconsView}
        <div id="icon_position_line" class="icon-position-line"></div>
      </ul>
    </div>
    <div class='window-manager'>
      {/*所有已打开窗口*/}
      <div class='windows'>{windowsView}</div>
    </div>
    {/*右键菜单*/}
    <ContextMenu
      manager={this.props.manager}
      desktopManagerCls={'desktopIcon-manager'}
      arrange={this.arrange}
      toggleAllWindows={this.toggleAllWindows}
    />

  </div>
</template>

<script>
export default {
  name: 'Desktop',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
