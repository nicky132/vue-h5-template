<template>
  <div ref="annularPie"></div>
</template>

<script>
import resize from '@/mixins/resize';
import echarts from 'echarts';

export default {
  name: 'annularPie',
  mixins: [resize],
  data() {
    return {};
  },
  mounted() {
    this.$nextTick(() => {
      this.initEchart();
    });
  },
  methods: {
    initEchart() {
      this.myChart = echarts.init(this.$refs.annularPie);
      this.myChart.setOption(
        {
          tooltip: {
            trigger: 'item'
          },
          legend: {
            show: true,
            left: '15',
            top: 0,
            type: 'scroll',
            itemWidth: 18,
            itemHeight: 11,
            data: ['TS', 'JS', 'Eslint', 'Babel']
          },
          series: [
            {
              name: 'TS',
              type: 'pie',
              hoverAnimation: false,
              radius: ['63%', '70%'],
              center: ['50%', '53%'],
              itemStyle: {
                normal: {
                  color: '#4FD8FF',
                  label: {
                    show: false
                  },
                  labelLine: {
                    show: false
                  }
                }
              },
              data: [
                {
                  value: 85,
                  name: 'TS'
                },
                {
                  value: 15,
                  name: '',
                  itemStyle: {
                    color: '#dedede'
                  },
                  hoverAnimation: false,
                  tooltip: {
                    show: false
                  }
                }
              ]
            },
            {
              name: 'JS',
              type: 'pie',
              hoverAnimation: false,
              radius: ['51%', '58%'],
              center: ['50%', '53%'],
              itemStyle: {
                normal: {
                  color: '#C15FFF',
                  label: {
                    show: false
                  },
                  labelLine: {
                    show: false
                  }
                }
              },
              data: [
                {
                  value: 75,
                  name: 'JS'
                },
                {
                  value: 25,
                  name: '',
                  itemStyle: {
                    color: '#dedede'
                  },
                  hoverAnimation: false,
                  tooltip: {
                    show: false
                  }
                }
              ]
            },
            {
              name: 'Eslint',
              type: 'pie',
              hoverAnimation: false,
              radius: ['39%', '46%'],
              center: ['50%', '53%'],
              itemStyle: {
                normal: {
                  color: '#FF5F55',
                  label: {
                    show: false
                  },
                  labelLine: {
                    show: false
                  }
                }
              },
              data: [
                {
                  value: 65,
                  name: 'Eslint'
                },
                {
                  value: 35,
                  name: '',
                  itemStyle: {
                    color: '#dedede'
                  },
                  hoverAnimation: false,
                  tooltip: {
                    show: false
                  }
                }
              ]
            },
            {
              name: 'Babel',
              type: 'pie',
              hoverAnimation: false,
              radius: ['27%', '34%'],
              center: ['50%', '53%'],
              itemStyle: {
                normal: {
                  color: '#FFC935',
                  label: {
                    show: false
                  },
                  labelLine: {
                    show: false
                  }
                }
              },
              data: [
                {
                  value: 65,
                  name: 'Babel'
                },
                {
                  value: 35,
                  name: '',
                  itemStyle: {
                    color: '#dedede'
                  },
                  hoverAnimation: false,
                  tooltip: {
                    show: false
                  }
                }
              ]
            }
          ]
        },
        true
      );
    }
  }
};
</script>
