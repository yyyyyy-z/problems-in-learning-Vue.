# problems-in-learning-Vue.
前端开发过程中遇到的问题，Vue结合element组件  
#### el-radio数据回显问题  
>问题：添加、修改功能可正常使用，但radio组件数据不能正常回显  
     如果原本数据是闲置，那么修改的时候，闲置不可以选择了， 也就是说，这个回显只是页面没有显示出来。  
![image](https://github.com/user-attachments/assets/b4e9a28d-497f-4579-9285-5579a48a6955)   
问题原因和解决方法：dict.value是字符串类型，通过*1 JavaScript 会尝试将其转换为数字类型
![image](https://github.com/user-attachments/assets/36f11105-e5d7-4e0d-bde8-7c096ea39ef9)回显正常
