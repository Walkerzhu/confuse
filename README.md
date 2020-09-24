# confuse(iOS马甲包，上架神器)

<a name="X50Qx"></a>
#                             ![image.png](https://cdn.nlark.com/yuque/0/2020/png/213807/1593768128247-016fe60b-8853-48fb-8b76-f9f702b83db5.png#align=left&display=inline&height=177&margin=%5Bobject%20Object%5D&name=image.png&originHeight=512&originWidth=512&size=119707&status=done&style=none&width=177)
<a name="4OMtJ"></a>
# 前言
因公司发展需要，本人19年中旬开始从事iOS马甲包业务，前期也使用过目前市面上其他得马甲包工具，均失败了。经过大量实践，开发出一款功能齐全的马甲包工具（支持OC、Lua、C++）。工具的主要功能OC已封装成Mac应用，其他功能还在封装中，敬请期待。（目前公测阶段: _**免费**_）
<a name="iji4j"></a>
# 实践
本人在实践中提审的结果汇总如下（涉及保密，不便透露细节）：

- 非游戏类过包率：**30~50%**
   - 优惠券类型18套，过包率42%
   - 壁纸类型15套，过包率33%
- 游戏类过包率：**20~30%**
   - 塔防类型约40套，过包率22%，该款游戏其他渠道方也在提审，历史提包总数预计500~1000套
   - 卡牌类型1套，过包率100%
<a name="8cWfW"></a>
# 功能
confuse是一款马甲包工具，侧重于**游戏马甲包**，尽最大可能模拟人工手动混淆，避免机器审核4.3、2.1、2.3.1、账号调查等，功能如下：

1. 混淆前资源替换，指定需要替换的资源文件夹，自动进行同名文件替换，方便快捷
1. 删注释
1. 魔改颜色，对项目中UI颜色随机偏移，可自定义宏
1. 微调字体，对项目中使用的字体随机微调，可自定义宏
1. 修改全局变量，替换全局变量名、混淆字符串变量值
1. 修改图片，图片质量修改、大小偏移、颜色微调、透明度设置、RGB偏移、模式修改等
1. 修改Log输出，智能替换
1. 修改URL，模拟人工近似替换
1. 重命名方法名，支持**多参修改**，近似Xcode的Rename功能，方法名混淆和类名及类型关联，同名方法不同类、同类同名方法不同类型（类方法、对象方法）混淆后将不一致
1. 重命名属性名，支持@property的对象、常量、block等所有类型，可设置属性名后缀过滤、**支持近似替换**
1. **修改方法**：拆分方法，对原方法进行封装并根据参数不同进行局部调整，然后调用
1. 重命名图片名
1. UI布局偏移，支持SDAutoLayout、Masonry、Frame
1. 垃圾垃圾，支持自动插入项目中，无需手动导入
   1. 插入ViewController文件
   1. 插入文本文件（json、txt、doc）
   1. 插入垃圾属性
   1. 插入垃圾方法
      1. 插入自定义垃圾文件
      1. 插入分类附带随机方法
15. 多语言混淆、支持汉字
15. 修改字符串，加密处理
15. xib、storyboard文件插入垃圾视图，并修改内部结构属性
15. 重命名文件名、类名，**支持近似替换**，可指定添加前缀
15. 修改项目基本配置，版本号、SDK的BundleID、版本号



以上所有功能均支持黑名单过滤，对指定的内容进行屏蔽，忽略混淆。各个模块的随机单词个数可自定义调整
<a name="vlfzY"></a>
# 图文介绍
运行APP效果图，使用前请详细阅读[工具使用教程](https://www.yuque.com/docs/share/edd2603f-d09d-4795-ae71-b42419b99446?#《confuse使用说明》)<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/213807/1594644980313-b3ee8604-9652-4bba-bb18-3d06399593e9.png#align=left&display=inline&height=540&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1080&originWidth=1920&size=537018&status=done&style=none&width=960)
<a name="WtuYs"></a>
# 更新日志
<a name="DZQQV"></a>
#### v1.7.0更新:

1. 重构插入方法
   1. ~~移除：项目中插入固定的文件并在每个方法中随机调用固定文件内的方法，原因：混淆太明显~~
   1. ~~移除：插入简单的随机代码块，原因：混淆太明显~~
   1. **新增**：每个类中创建分类（Category）,并插入随机方法，后期将进一步升级


<br />[查看更多历史更新记录](https://www.yuque.com/docs/share/39f2f60e-b6a8-443b-b005-b9364fb79b95?#《confuse更新说明》)
<a name="2uJ0e"></a>
# 链接导航

1. [马甲包简介](https://www.yuque.com/docs/share/7e70244c-5dea-4035-b634-65cc082097da?#《马甲包简介》)
