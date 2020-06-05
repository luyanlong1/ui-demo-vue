<template>
    <div class="top-middle-cmp">
        <div class="chart-name">
            任务达成率月趋势
        <dv-decoration-3 style="width:200px;height:20px;" />
        </div>
        <dv-charts :option="option" style="margin-top:10px;margin-left:15px" />
    </div>
</template>

<script>
export default {
    name: 'TopMiddleCmp',
    data () {
        return {
        option: {
            legend: {
                data: ['任务达成率'],
                textStyle: {
                    fill: '#fff'
                }
            },
            xAxis: {
                data: [
                    '06/01  ', '06/02  ', '06/03  ', '06/04  ', '06/05  ', '06/06  ',
                    '06/07  ', '06/07  ', '06/08  ', '06/09  ', '06/10  ', '06/11  ',
                    '06/12  ', '06/13  ', '06/14  ', '06/15  '
                ],
                boundaryGap: false,
                axisLine: {
                    style: {
                        stroke: '#999'
                    }
                },
                axisLabel: {
                    style: {
                        fill: '#999',
                        rotate : -60 
                    }
                },
                axisTick: {
                    show: false
                }
            },
            yAxis: {
                data: 'value',
                splitLine: {
                    show: false
                },
                axisLine: {
                    style: {
                    stroke: '#999'
                    }
                },
                axisLabel: {
                    style: {
                    fill: '#999'
                    },
                    formatter ({ value }) {
                    return value.toFixed(2)
                    }
                },
                axisTick: {
                    show: false
                },
                min: 95,
                max: 100,
                interval: 0.5
            },
            series: [
            {
                data: [
                99.56, 99.66, 99.84, 99.22, 99.11, 99.45,
                99.44, 99.81, 99.84, 99.32, 99.14, 99.45,
                99.15, 99.45, 99.64, 99.89
                ],
                type: 'line',
                name: '任务达成率',
                smooth: true,
                lineArea: {
                show: true,
                gradient: ['rgba(55, 162, 218, 0.6)', 'rgba(55, 162, 218, 0)']
                },
                linePoint: {
                radius: 4,
                style: {
                    fill: '#00db95'
                }
                }
            }
            ]
        }
        }
    }
}
</script>
<style lang="less">
.top-middle-cmp {
    position: relative;
    padding: 0 50px;
    box-sizing: border-box;

    .chart-name {
        position: absolute;
        right: 70px;
        text-align: right;
        font-size: 20px;
        top: 10px;
    }
}
</style>