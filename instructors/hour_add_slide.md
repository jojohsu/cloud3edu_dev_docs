### 创建课件@Slide管理
* 响应式设计，响应宽度范围1280px至1920px；左侧Nav宽度不变，右侧Slide Nav宽度不变，主区域随WindowsSize变化。
* 当切换课时，则当前课时任何合法字段自动保存，非法字段丢弃，再次进入该课时显示课时dashboard。
* 左侧课时根据课程创建时的课时安排自动生成全部课时。
* 点击当前slide自动预载入后2张slide。

##### 左侧课程导航
* 课程名默认为课程1，课程2升序，课程名会根据右侧Title输入结果动态反馈。
* Title超过1行自动折行。

##### 右侧Title
* Lesson Dropdown可自由选择课时，选择后会在左侧导航插入对应的课时。如：当前有3个课时，如果将当前的Lesson 3改为Lesson 4，会在Lesson 2下自动追加Lesson 3课时，如将当前课时改为Lesson 3，会自动删除自动生成的Lesson 3课时；下拉内容仅支持3个课时（包括当前课时），如当前Lesson 3，下拉列表为Lesson 3、Lesson 4、Lesson 5。
* Title不能为空，长度在1-40个字节，Placeholder：请输入当前课时的名称。

##### Slide
* Slide responsive规则：slide宽度超出容器宽度、slide高度小于容器高度，则同比缩放至容器宽度；slide高度超出容器高度、slide宽度小于容器宽度，则同比缩放至容器高度。
* 点击slide在容器内以原图大小1:1显示，超出容器部分显示上下滚动条；再次点击后回到上一状态。

##### 添加问题
* 当任何textarea或input内value变化，该input或textarea blur之后，在function区域显示已保存。
* 合法问题数据为textare内容＋图片 ／ textarea内容 ／ 图片，不满足这3种情况为非法数据，出现提示：请输入问题或上传问题图片。
* 问题textarea placeholder：请输入问题；问题长度1-1000个字符。
* Textarea高度固定，value垂直居中，超出高度出现滚动条。

##### 添加问题@上传图片
* 通过问题旁的upload icon触发OS upload frame，选择合法图片（png、gif、jpg）后进入crop界面；选择非法文件时给出提示：暂不支持你选择的文件格式。
* crop界面右侧显示actual size的preview，该区域宽高度固定；左边显示crop后的实时preview，该区域高度固定，宽度responsive。
* 点击删除回到初始界面，文字信息保留，点击完成进入preview界面。在preview界面中，高度固定，上传的图片点击后放大，放大逻辑同slide。

##### 选择题
* 默认创建3个选项，选项textarea内无内容时该选项置灰，正确答案的check标识不出现，上课时不出现该选项；当有内容时，选项active，出现正确答案的check按钮。
* 最少2个选项，A、B选项的placeholder：请输入选项，该选项必填；B选项之后的选项placeholder：请输入选项，留空则选项X不会显示；选项长度1-300个字符。
* 选项答案的颜色依次为：#F16C47、#F1AE47、#3DBF12、#08B570、#0888B5、#8E08B5、#B5086A，超过7个选项则从第一个选项开始循环。

##### 排序题
* 默认创建3个选项，最少2个选项；选项textarea内无内容时该选项置灰，上课时不出现该选项。
* 最少2个选项，前两个选项的placeholder：请输入排列项，该选项必填，选项长度1-300个字符。
* 选项头的竖线默认不显示，hover到选项的整行时显示，鼠标移到选项头浅蓝色底区域cursor变为move，拖动该区域可对选项进行排序。

##### Slide Nav
* 在Slide thumbnail区域及下方padding区域Hover，出现添加问题btn及show btn
* Trigger show btn后当前slide thumbnail被遮罩，上课时不显示隐藏的slide。
* 点击thumbnail时，如果当前处于问题编辑状态，则将问题数据提交。