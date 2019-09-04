<template>
  <div class="main">
    <div class="mainBox">
      <div class="mainBoxHead">
        <p><img src="../components/images/zhuyi.png" width="28px">本问卷能帮您选择购买最合适的保险产品，请如实填写信息</p>
      </div>
      <div class="listBox">
        <div class="itme">
            <div class="question">1. 您和您的家人已经获得的保险保障有哪些？</div>
            <div class="answer">
              <van-radio-group v-model="radio">
                <van-radio name="1">单选框 1</van-radio>
                <van-radio name="2">单选框 2</van-radio>
              </van-radio-group>
              <van-checkbox-group v-model="result">
                <van-checkbox
                  v-for="(item, index) in list"
                  :key="item"
                  :name="item"
                >
                  复选框 {{ item }}
                </van-checkbox>
              </van-checkbox-group>
            </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        radio: '1',
        checked: true,
        list_a: [
          {'type': 1, 'name': 'one', 'question': '您和您的家人已经获得的保险保障有哪些？', 'answer': [{'value': '社会保险'}, {'value': '商业保险'}]},
          {'type': 1, 'name': 'two', 'question': '您和您的家人已经获得的保险保障有哪些？', 'answer': [{'value': '社会保险'}, {'value': '商业保险'}]},
          {'type': 1, 'name': 'three', 'question': '您和您的家人已经获得的保险保障有哪些？', 'answer': [{'value': '社会保险'}, {'value': '商业保险'}]},
          {'type': 1, 'name': 'four', 'question': '您和您的家人已经获得的保险保障有哪些？', 'answer': [{'value': '社会保险'}, {'value': '商业保险'}]},
          {'type': 2, 'name': 'five', 'question': '您和您的家人已经获得的保险保障有哪些？', 'answer': [{'value': '社会保险'}, {'value': '商业保险'}, {'value': '社会保险'}, {'value': '商业保险'}]}
        ],
        result: ['a', 'b'],
        list: ['a', 'b', 'c']
      }
    },
    mounted(){
    },
    methods:{

    },
    components:{

    }
  }
</script>
<style lang="stylus" rel="stylesheet/stylus" scoped>
  @import "../common/stylus/variable.styl"
  @import "../common/stylus/mixin.styl"
  .main,.mainBox
    width 100%
  .mainBoxHead
    line-height 37px
    font-size 12px
    color #FF7900
    padding-left 18px
    background #EEEEEE
  .mainBoxHead p img
    width 14px
    vertical-align text-top
    margin-right 7px
  .listBox
    padding-left 15px
    margin-top 30px
  .itme .question
    color #555
    font-size 15px
</style>
