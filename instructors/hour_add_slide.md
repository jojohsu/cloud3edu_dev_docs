### 创建课件@Slide管理
* 响应式设计，响应宽度范围1280px至1920px；左侧Nav宽度不变，右侧Slide Nav宽度不变，主区域随WindowsSize变化。
* 当切换课时，则当前课时任何字段自动保存。
* 左侧课时根据课程创建时的课时安排自动生成全部课时。
* 点击当前slide自动预载入后2张slide。

##### 左侧课程导航
* 课程名默认为课程1，课程2升序，课程名会根据右侧Title输入结果动态反馈。
* Title超过1行自动折行。

##### 右侧Title
* Lesson Dropdown可自由选择课时，选择后会在左侧导航插入对应的课时。如：当前有3个课时，如果将当前的Lesson 3改为Lesson 4，会在Lesson 2下自动追加Lesson 3课时，如将当前课时改为Lesson 3，会自动删除自动生成的Lesson 3课时；下拉内容仅支持3个课时（包括当前课时），如当前Lesson 3，下拉列表为Lesson 3、Lesson 4、Lesson 5。
* Title不能为空，长度在1-40个字节，Placeholder：请输入当前课时的名称。

##### 添加问题
* 当任何textarea或input内value变化，该input或textarea blur之后，在function区域显示已保存。
* 合法问题数据为textare内容＋图片 ／ textarea内容 ／ 图片，不满足这3种情况为非法数据，出现提示：请输入问题或上传问题图片。
* 问题textarea placeholder：请输入问题；问题长度1-1000个字符。
* Textarea高度固定，value垂直居中，超出高度出现滚动条。

##### 添加问题@上传图片


##### 选择题
* 默认创建3个选项，选项textarea内无内容时该选项置灰，正确答案的check标识不出现，上课时不出现该选项；当有内容时，选项active，出现正确答案的check按钮。
* 最少2个选项，A、B选项的placeholder：请输入选项，该选项必填；B选项之后的选项placeholder：请输入选项，留空则选项X不会显示；选项长度1-300个字符。
* 选项答案的颜色依次为：#F16C47、#F1AE47、#3DBF12、#08B570、#0888B5、#8E08B5、#B5086A，超过7个选项则从第一个选项开始循环。

##### Slide Nav
* 在Slide thumbnail区域及下方padding区域Hover，出现添加问题btn及show btn
* Trigger show btn后当前slide thumbnail被遮罩，上课时不显示隐藏的slide。
* 点击thumbnail时，如果当前处于问题编辑状态，则将问题数据提交。