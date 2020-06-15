<template>
    <div>
        <div ref="echarts" class="echarts">

        </div>
    </div>
</template>

<script>
    export default {
        name: "Pie",
        data() {
            return {
                // echartsData:[
                //     {value: 335, name: '直接访问'},
                //     {value: 310, name: '邮件营销'},
                //     {value: 274, name: '联盟广告'},
                //     {value: 235, name: '视频广告'},
                //     {value: 400, name: '搜索引擎'}
                // ],
                options: {
                    backgroundColor: '#2c343c',
                    title: {
                        text: "ECharts 入门示例"
                    },
                    tooltip: {},
                    // legend: {
                    //     data: ["销量"]
                    // },
                    // xAxis: {
                    //     data: ["衬衫", "羊毛衫", "雪纺衫", "裤子", "高跟鞋", "袜子"]
                    // },
                    // yAxis: {},
                    series: [
                        {
                            type: "pie",
                            radius: '55%',
                            center: ['50%', '50%'],
                            data: [
                                {value: 335, name: '直接访问'},
                                {value: 310, name: '邮件营销'},
                                {value: 274, name: '联盟广告'},
                                {value: 235, name: '视频广告'},
                                {value: 400, name: '搜索引擎'}
                            ],

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
    .echarts{
        height: 500px;
        width: 500px;
    }
</style>
