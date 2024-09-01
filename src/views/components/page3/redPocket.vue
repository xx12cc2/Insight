<template>
    <div class="redPocket"></div>
</template>

<script>
export default {
    name: 'redPocket',
    data() {
        return {}
    },
    methods: {
        // 红包装账
        setPocket() {
            let option = {
                tooltip: {
                    trigger: 'axis',
                    axisPointer: {            // 坐标轴指示器，坐标轴触发有效
                        type: 'shadow'        // 默认为直线，可选为：'line' | 'shadow'
                    },
                },
                title: {
                    text: "通话时间分析",
                    top: "6%",
                    left: '2%',
                    textStyle: {
                        color: '#fff',
                        fontSize: 14
                    }
                },
                grid: {
                    top: "23%",
                    bottom: '10%'
                },
                xAxis: {
                    scale: true,
                    name: '时长',
                    nameTextStyle: {
                        color: "#0FB9CD",
                        fontSize: 10
                    },
                    axisLine: {
                        show: false
                    },
                    axisLabel: {
                        color: '#0FB9CD',
                        fontSize: 8
                    },
                    axisTick: {
                        color: '#14336D'
                    },
                    splitLine: {
                        lineStyle: {
                            color: '#14336D'
                        }

                    }

                },
                yAxis: {
                    scale: true,
                    name: '时间',
                    nameTextStyle: {
                        color: "#0FB9CD",
                        fontSize: 10,
                        padding: [0, 65, -10, 0]
                    },
                    axisTick: {show: false},
                    axisLabel: {
                        color: '#0FB9CD',
                        fontSize: 8
                    },
                    axisLine: {
                        lineStyle: {
                            color: '#134076'
                        }
                    },
                    splitLine: {
                        lineStyle: {
                            color: '#14336D'
                        }
                    }
                },
                series: [{
                    type: 'effectScatter',
                    symbolSize: 10,
                    z: 10,
                    itemStyle: {
                        color: '#FF1200'
                    },
                    data: [
                        [172.7, 10],
                        [153.4, 18]
                    ]
                }, {
                    type: 'scatter',
                    itemStyle: {
                        color: '#0E4CFF'
                    },
                    data: [
                      [162.8, 16.4], [167.0, 16.9], [60.0, 14.5], [160.0, 19.7], [168.9, 8.8],
                      [158.2, 13.4], [156.0, 10.1], [160.0, 16.9], [67.1, 9.1], [158.0, 9.8],
                      [122.6, 16.5], [26.0, 14.7], [162.1, 12.2], [133.4, 15.0], [59.8, 16.4],
                      [70.5, 14.4], [159.2, 9.7], [57.5, 11.2], [61.3, 14.6], [132.6, 10.1],
                      [60.0, 12.0], [168.9, 16.7], [65.1, 10.1], [132.6, 11.7], [165.1, 11.2],
                      [66.4, 12.9], [60.0, 14.2], [52.4, 8.4], [140.2, 11.0], [12.6, 19.9],
                      [70.2, 12.9], [158.8, 15.4], [112.7, 19.4], [67.6, 8.6], [162.6, 8.0],
                      [87.6, 18.1], [56.2, 10.0], [175.2, 19.5], [72.1, 15.2], [162.6, 9.7],
                      [90.0, 11.0], [165.1, 12.7], [102.9, 10.5], [66.4, 17.1], [125.1, 19.5],
                      [102.7, 19.9], [101.3, 10.5], [167.6, 19.7], [65.1, 11.0], [157.5, 10.0],
                      [63.8, 14.3], [67.6, 15.2], [65.1, 16.6],

                    ],
                },
                    {
                        type: 'scatter',
                        itemStyle: {
                            color: '#2E62F9'
                        },
                        data: [[161.2, 15.8], [127.5, 13.5], [159.5, 13.8], [17.0, 17.3], [155.8, 15.4],
                          [170.0, 12.7], [19.1, 17.9], [166.0, 17.5], [116.2, 13.4], [160.2, 18.5],
                          [172.5, 10.9], [110.9, 14.8], [12.9, 12.1], [153.4, 14.4], [110.0, 11.2],
                          [10.2, 8.4], [88.2, 9.3], [175.0, 9.8], [157.0, 13.4], [67.6, 10.7],
                          [159.5, 9.1], [175.0, 19.9], [86.8, 9.1], [96.5, 11.5], [90.2, 8.7],
                          [174.0, 9.9], [173.0, 17.3], [179.9, 8.2], [110.5, 14.0], [60.0, 16.9],
                          [154.4, 19.9], [82.0, 16.9], [86.5, 19.4], [10.0, 8.8], [52.0, 12.9],
                          [162.1, 15.6], [170.0, 9.1], [60.2, 17.6], [121.3, 12.0], [116.4, 12.6],

                        ],
                    }]
            };
            let myChart = this.$echarts(this.$el);

            myChart.clear();
            myChart.resize();
            myChart.setOption(option);
        },
    }, mounted() {
        this.setPocket();
    },
}
</script>

<style lang="less" scoped>
.redPocket {
    height: 100%
}
</style>