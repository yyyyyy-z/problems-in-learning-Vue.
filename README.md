# problems-in-learning-Vue.
前端开发过程中遇到的问题，Vue结合element组件  
#### el-radio数据回显问题  
>问题：添加、修改功能可正常使用，但radio组件数据不能正常回显  
     如果原本数据是闲置，那么修改的时候，闲置不可以选择了， 也就是说，这个回显只是页面没有显示出来。  
![image](https://github.com/user-attachments/assets/b4e9a28d-497f-4579-9285-5579a48a6955)   
问题原因和解决方法：dict.value是字符串类型，通过*1 JavaScript 会尝试将其转换为数字类型
![image](https://github.com/user-attachments/assets/36f11105-e5d7-4e0d-bde8-7c096ea39ef9)回显正常
#### el-table-column表格字段实现权限控制
>问题：因为一些需求，有些字段需要隐藏给指定用户  
>![image](https://github.com/user-attachments/assets/be5c9218-606c-47a4-81b9-a886f9255668)  
解决方法： 引用$auth（Vue插件提供的全局属性），hasPermi方法检查用户权限的逻辑实现，它可能从Vuex存储、本地存储、会话存储或后端API中获取用户的权限信息。
![image](https://github.com/user-attachments/assets/f555c4e8-46a3-4c3c-8a69-dcb35c89f45d)
![image](https://github.com/user-attachments/assets/e7d1b9e0-942c-468b-ac2d-014220909386)在没有授权的角色中该字段已隐藏
#### el-table 表格中多个数组元素用逗号隔开显示  
>![image](https://github.com/user-attachments/assets/94ba9cef-689c-42ea-9653-89dfd81c614c)  
scope.row.userName 是该行的 userName 数据。假设 userName 是一个数组，join(",") 会把数组中的所有元素连接成一个字符串，并用逗号 , 分隔开。  
效果展示  
![image](https://github.com/user-attachments/assets/1fc88a37-bdee-4621-a0ee-3e44d4ebf0a0)
