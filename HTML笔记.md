# 九大HTML常用标签
> ## 1. h1 ~ h6 //**标题标签**
> ## 2. div 和 span //**大小分区标签**
>     - 每个div独占一行
>     - 一行可以占领多个span
> ## 3. p //**段落标签**
> ## 4. &lt;img src="图片路径" alt="图像不显示时用文字替换" title="提示，鼠标悬停时显示的文字">
> ## 5. &lt;ul> and &lt;ol> and &lt;dl> //**列表标签**
>     - ul为无序列表,内包含&lt;li>
>     - ol为有序列表,内包含&lt;li>
>     - dl为自定义列表,内包含&lt;dt>、&lt;dd>
>     ```
>     <dl>
>       <dt>名词1</dt>
>       <dd>名词1解释1</dd>
>       <dd>名词1解释2</dd>
>     </dl>
>     ```
> ## 6. &lt;a href="跳转目标" target="目标窗口的弹出方式">文本或图像&lt;/a> //**超链接**
>     - target 打开窗口的方式 默认为 **_self** 在当前的窗口打开 **_blank** 在新窗口打开
>     - **锚点链接:** ----可以用来做快速返回顶部的操作
>    > - 设置属性值为 **#名字** 的形式，如： &lt;a href="#跳转名称">跳转地点&lt;/a>
>    > - 找到目标位置标签，里面添加一个**id**属性 = 刚才的名字，如：&lt;h3 id="跳转名称">跳转地点内容&lt;h3>
> ## 7. table //**定义表格标签**
>     - tr //**定义行标签,必须嵌套在&lt;table>&lt;/table>中**
>     - td //**定义表格中的单元格,必须嵌套在&lt;tr>&lt;/tr>中**
>     - th //**表示表头部分,可以加粗和居中显示**
>     - thead //**表格的头部区域,可以把&lt;tr>包含在里面,主要起划分作用**
>     - tbody //**表格的主题区域,可以把&lt;td>包含在里面,主要起划分作用**
>    
>    | 属性名 | 属性值 | 描述 |
>    | :--- | :--- | :--- |
>    | align | left、center、right | 表格周围元素的对齐方式 |
>    | border | 1或"" | 表格单元是否拥有边框,默认为"" |
>    | cellpadding | 像素值 | 单元边沿与其内容之间的空白,默认1像素 |
>    | cellspacing | 像素值 | 单元格之间的空白,默认2像素 |
>    | width | 像素值或百分比 | 表格的宽度 |
>    >**合并单元格**
>    > 1. 合并方式:跨行合并(rowspan)、跨列合并(colspan)
>    > 2. 找到目标单元格. **合并方式=合并单元格数量 &nbsp;&nbsp;如: &lt;td colspan="2">&lt;/td>**
>    > 3. 删除多余的单元格
> ## 8. from //**定义表单域,以实现用户信息的收集和传递**
>     ```
>     <form action="url地址" methor="提交方式" name="表单域名称">
>       各种表单元素控件
>     </from>
>     ```
>    | 属性名 | 属性值 | 描述 |
>    | :--- | :--- | :--- |
>    | action | url地址 | 指定接收并处理表单数据的服务器程序的url地址 |
>    | method | get/post | 设置表单数据的提交方式,其取值为get或post |
>    | name | 名称 | 指定表单的名称,以区分同一个页面中的多个表单域 |
>    > ### **&lt;input>表单元素**
>    > > 语法：
>    > > ```
>    > > <input type="属性值" name="input元素名称" value="input元素的值" checked="此input元素首次加载时应当被选中" maxlength="输入字段中的字符的最大长度" />
>    > > ```
>    > > **单选按钮和复选框一般要有相同的name**
>    > > 
>    > > **checked="checked" 表示打开页面时，标签已经选中了**
>    > > 
>    > > type的属性值表：
>    > > | 属性值 | 描述 |
>    > > | :--- | :--- |
>    > > | button | 定义可点按钮（多数情况下，用于通过JavaScript启动脚本） |
>    > > | checkbox | 定义复选框 |
>    > > | file | 定义输入字段和“浏览”按钮，供文件上传 |
>    > > | hidden | 定义隐藏的输入字段 |
>    > > | image | 定义图像形式的提交按钮 |
>    > > | password | 定义密码字段，该字段中的字符被掩码 |
>    > > | radio | 定义单选框 |
>    > > | reset | 定义重置按钮，重置按钮会清除表单中的所有数据 |
>    > > | submit | 定义提交按钮，提交按钮会把表单数据发送到服务器 |
>    > > | text | 定义单选的输入字段，用户可在其中输入文本，默认宽度为20个字符 |
>    > > 
>    > > &lt;label> //**为input元素定义标注**
>    > > 可以绑定表单元素，比如把光标选中文字就可以自动将焦点转移到对应的选项上，增加用户体验
>    > > 语法：
>    > > ```
>    > > <label for="input中的id属性">男</label>
>    > > <input type="radio" name="sex" id="sex" />
>    > > ```
>    > > 核心：&lt;label>的**for属性的属性值应当与相关元素的id属性值相同**
>    > ### &lt;select> //**下拉表单元素**
>    > > ```
>    > > <select>
>    > >  <option>选项1</option>
>    > >  <option>选项2</option>
>    > >  <option>选项3</option>
>    > > </select>
>    > > ```
>    > > **在&lt;option>中定义selected="selected"时，当前项即为默认选中项**
>    > ### &lt;textarea> //**文本域元素，可以提供一个类似于评论栏的元素**
>    > > 语法：
>    > > ```
>    > > <textarea cols="每行中的字符数" row="显示的行数">
>    > >  默认文本内容
>    > > </textarea>
>    > > ```
>    > > 
