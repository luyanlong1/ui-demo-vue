<template>
  <div class="bottom-right-table-2">
    <dv-border-box-6>
      <div class="table-name">
        <img src="./img/icon2.png" />系统bug排行榜
      </div>

      <dv-scroll-board :config="config" />
    </dv-border-box-6>
  </div>
</template>

<script>
export default {
  name: 'BottomRightTable2',
  data () {
    return {
      config: {
        data: [
          ['业务逻辑不通', '月累计：4起'],
          ['代码逻辑错误', '月累计：3起'],
          ['SQL逻辑问题', '月累计：3起'],
          ['编码规范不合规', '月累计：3起'],
          ['编码遗漏', '月累计：2起'],
          ['业务梳理不清楚', '月累计：1起']
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
.bottom-right-table-2 {
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
