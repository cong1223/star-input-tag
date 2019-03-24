# star-input-tag
基于elementui Tag标签，增加了原有标签的编辑功能


1. 引入组件
```import starInputTag from '...'```
2. 注册组件
```
components: {
      starInputTag
}
```
3. 使用组件
```<star-input-tag />```
- v-model 标签内容，数组或者字符串，字符串每个标签以逗号隔开
- theme  新增按钮名称
- created(){   字符串转数组，定义在父组件
	if(typeof this.tagList =='string'){
		this.tagList = this.tagList.split(',');
	}
},
---
###示例：
```<star-input-tag v-model="tagList" theme="添加新标签" />```

```
data() {
     return {
          //tagList: ['自定义标签一','自定义标签二','自定义标签三'],
          tagList: "自定义标签一,自定义标签二,自定义标签三"
          }
 }
```
如果需要穿字符串：
```
created(){
      if(typeof this.tagList =='string'){
         this.tagList = this.tagList.split(',');
      }
},
 ```
