<template>
    <div >
        222222
        <div ref="echarts" class="echart-container">

        </div>
    </div>
</template>

<script>
    export default {
        name: "Start",
        data() {
            return {
                options: {
                    title: {
                        text: "ECharts 入门示例"
                    },
                    tooltip: {},
                    legend: {
                        data: ["销量"]
                    },
                    xAxis: {
                        data: ["衬衫", "羊毛衫", "雪纺衫", "裤子", "高跟鞋", "袜子"]
                    },
                    yAxis: {},
                    series: [
                        {
                            name: "销量",
                            type: "bar",
                            data: [5, 20, 36, 10, 10, 20]
                        }
                    ]
                }
            }
        },
        mounted() {
            this.createEcharts()
        },
        methods: {
            createEcharts() {
                let myChat = this.$echarts.init(this.$refs.echarts);
                myChat.setOption(this.options)
            }
        },
    }
</script>

<style scoped lang="scss">
    .echart-container{
        height: 300px;
        width: 300px;
    }
</style>
