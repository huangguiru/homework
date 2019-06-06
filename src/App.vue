<template>
  <!-- vue的模板里面 所有的内容要被一个根节点包含起来 -->
  <div id="app">
      <h2>你好vue---{{msg}}</h2>
      <br>
      这是根主件
      <h3>{{obj.name}}</h3>
      <br>
      <hr>

      <ul>
        <li v-for="item in list"> {{item}}</li>
      </ul>
      <br>
      <hr>

      <ul>
        <li v-for="item in list1"> {{item.title}}</li>
      </ul>
      <br>
      <hr>
      <ul>
          <li v-for="item in list2"> {{item.cate}}
            <ol>
              <li v-for="news in item.list3">{{news.title}}</li>
            </ol>
          </li>
        </ul>


  </div>
</template>

<script>
export default {
  name: 'app',
  data () {/*业务逻辑里面定义的数据*/
    return {
      msg: '你好vue',
      obj:{
        name:"黄桂茹1"
      },
      list:['林志颖','黄子华','周慧敏'],
      list1:[
        {'title':'香蕉'},
        {'title':'苹果'},
        {'title':'梨子'},
        {'title':'龙眼'},
      ],
      list2:[
        {
          "cate":"国内新闻",
          "list3":[
            {'title':'国内新闻民生'},
            {'title':'国内新闻教育'},
          ]
        },
        {
          "cate":"国际新闻",
          "list3":[
            {'title':'科技新闻'},
            {'title':'国防安全'},
          ]
        }
      ]
    }
  }
}
</script>

<style lang="scss">

</style>
