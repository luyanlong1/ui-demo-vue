<template>
  <div class="bottom-right-table-4">
    <dv-border-box-6>
      <div class="table-name">
        <img src="./img/icon4.png" />系统新功能排行榜
      </div>

      <dv-scroll-board :config="config" />
    </dv-border-box-6>
  </div>
</template>

<script>
export default {
  name: 'BottomRightTable4',
  data () {
    return {
      config: {
        data: [
          ['审批系统', '月累计：4起'],
          ['好差评系统', '月累计：3起'],
          ['认证系统', '月累计：3起'],
          ['事项系统', '月累计：3起'],
          ['服务调度系统', '月累计：2起'],
          ['其他', '月累计：1起']
        ],
        index: true,
        columnWidth: [30, 100],
        align: ['center'],
        oddRowBGC: 'rgba(9, 37, 50, 0.4)',
        evenRowBGC: 'rgba(10, 32, 50, 0.3)'
      }
    }
  }
}
</script>

<style lang="less">
.bottom-right-table-4 {
  width: calc(~"25% + 10px");
  height: 100%;
  margin: 0 -5px;

  .border-box-content {
    padding: 20px;
    box-sizing: border-box;
  }

  .table-name {
    height: 45px;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 15px;

    img {
      width: 40px;
      height: 40px;
      margin-right: 5px;
    }
  }

  .dv-scroll-board {
    height: calc(~"100% - 60px");
  }
}
</style>
