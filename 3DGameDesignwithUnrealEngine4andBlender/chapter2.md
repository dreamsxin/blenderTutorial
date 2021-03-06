现在是时候激动人心了！当我们继续构建我们的第一个项目时，我们将使用我们在上一章中讨论过的设计过程，并从一个水平草图开始。你可能想要打开虚幻引擎并向右跳，对吧？当我能够建立一个我一直想要的那个甜蜜水平的时候会花费多少时间？好吧，这就是原因。避免多次修订和花费大量时间重做级别部分的最佳方法是提前计划。弄清楚关卡的设置，架构，背景和故事。考虑一下你会在哪里放置故事提示和电源。由朋友，玩家和团队成员运行你的想法。记录你收到的反馈，然后建立你的级别。水平设计师相当于“测量两次，切一次”。

让我们来看看我们的关卡草图：

![关卡草图](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E5%85%B3%E5%8D%A1%E8%8D%89%E5%9B%BE.png)

所以这是我们的第一级。关卡本身非常基础。我们有两个房间通过走廊连接，一些楼梯通向第二层。在我们完成基本布局后，我们可以在侧面货物升降机，并为玩家进行互动。我试图以小型货船的形式布置水平，以适应我们科幻恐怖游戏的主题。该级别将作为设置的介绍，以及将玩家运送到我们稍后将建设的闹鬼空间站环境的方式。

在这一章，我们将包含下列主题：

*   Building the level using Unreal's Content Browser

*   Using different types of light

*   Adding interactive elements using Triggers and Blueprints

*   Playtesing our level

## Using the Content Browser to start building the level

继续打开Epic Games Launcher，拉出我们在最后一章末尾开始的项目。虚幻引擎4是对引擎最新版本的巨大升级，因为它为用户提供了一个简单的拖放界面。这是使用界面中的两个重要窗格完成的：Modes窗格和Content Browser。界面的这些部分允许关卡设计师将元素拖动到关卡中并将它们放置在需要的位置。在这两个中，我们将最多使用Content Browser

![内容浏览器](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E5%86%85%E5%AE%B9%E6%B5%8F%E8%A7%88%E5%99%A8.png)

Content Browser包含可在创建中使用的所有对象，声音，材质和粒子。它们被分类到镜像存储项目的文件结构的文件夹中。如果需要，Unreal会这样做以轻松移动项目文件。浏览浏览器很容易。双击文件夹会打开该文件夹，而面板的顶部会显示一个breadcrumb trail，可以单击该trail以向后移动你的选择。我想确保源面板也打开；这使得导航和查找特定文件更容易。当我们创建项目时，我们告诉Unreal包含Starter Content文件夹。此文件夹包含许多我们开始使用的基础知识，例如各种基本形状，建筑构件，材料等。有了这些，我们就可以开始对我们的设计进行白盒化。

从创建第一个房间开始：

![开始创建](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E5%BC%80%E5%A7%8B%E6%9E%84%E5%BB%BA.png)

要开始构建我们的第一个房间，我们将利用我们在Architecture文件夹中拥有的资产。通过选择地板，墙壁门，我们将组装我们设计的第一个房间

1. 首先让我们开始我们项目的新level。前往File菜单，单击它，然后选择新level。在出现的对话框中选择Empty。

2. 新level绝对没有任何内容。非常适合我们进军太空！放入Floor_400x400作为开始的地方。这是通过单击并从内容浏览器将片段拖动level来完成的。转到详细信息面板并确保其位置设置为x=0 y=0 z=0.这样可以轻松排列我们的其他作品。

3. 复制5次地板。这可以通过按住ALT并移动对象来创建副本来完成。将它们排列成2x3矩形，以创建一个大小合适的房间。

4. 接下来，让我们抓住一些墙。将Wall_400x300拖动到其中一个地板上的水平位置：

![房间](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E6%88%BF%E9%97%B4.png)

5. 我们将使用4-viewport视图排列我们的墙部分。在视口的右上角，有一排图标，用于控制多个不同的项目，例如网格捕捉，角度捕捉，缩放捕捉和相机速度。一直到这些图标右侧的是最小化/最大化按钮。单击该按钮可调出四个，将墙壁部分与地板一角对齐。

6. 复制墙部分，然后使用Move和Rotate工具封闭空间。

7. 最后，通过取出地板并将它们用作屋顶来完成房间来封闭空间。

在这一点上，我确定你只是想要跌入level并在你的新房间跑来跑去。但是，为了测试我们的level，我们需要添加一些东西：灯光和玩家开始。出于测试目的，让我们放入几个Pointights。转到屏幕左侧的Modes面板，然后将两个Pointights拖入你的房间。再次使用4-viewport配置确保它们位于你想要的位置。其次，在同一个面板中，拖动PlayerStart。PlayerStart的箭头从中心伸出。这就是玩家在spawn时将面临的方向。始终尝试将PlayerStart指向你希望玩家先行的方向。这就确保了玩家从一开始就参与其中，并且可以轻松地享受你的创作。最后，我们需要保存文件（使用File菜单或Ctrl+S)并使用Build按钮构建level。

在构建level时测试level是设计过程的重要部分。通过测试，你可以发现你的level是否存在任何缺陷或问题，并在事情变得过于复杂之前进行修复。要测试你的level，请按Play按钮。这将在当前视口中启动播放会话，并允许你在level中运行。如果单击Play按钮旁边的小向下箭头，你将可以选择打开其他类型的播放窗口，例如New Editor Window。能够看到整个播放屏幕会很有帮助。现在测试你的level并确保所有内容都正确排序。一旦你对你的第一个房间感觉良好，让我们构建其余的设计：

![其余设计](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E5%85%B6%E4%BD%99%E8%AE%BE%E8%AE%A1.png)

现在让我们建造走廊。我们可以通过复制我们的level的现有作品轻松构建我们的走廊。我还将向你展示如何在不删除它们的情况下交换片段中的片段：

1. 选择第一个房间中的一个地板块。复制它并将其排列在你想要将门口放入走廊空间的位置。

2.进入Content Browser并选择Wall_Door_400x300。我们将用这件作品替换其中一个墙壁部分。现在选择要在视口中替换的墙块。右键单击它，然后从菜单中选择Replace Selected Actors with Wall_Door_400x300.

![门替墙](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E9%97%A8%E6%9B%BF%E5%A2%99.png)

这将把现有的静态网格与我们选择的网格交换，并添加到那个完美尺寸的门口。复制地板部分两次以延长走廊。不要忘记确保所有部件与现有地板正确对齐。

4. 复制墙壁部分并将其添加到走廊。复制几次封闭走廊的长度。

5. 最后，复制地板以创建天花板并围绕你的走廊，并在其中添加一个灯。

建立你的level并给它一个测试。如果走廊感觉不够长，请添加几个部分。一旦你对目前的level感觉满意，请保存文件。现在让我们添加最后的房间

![最后的房间](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E6%9C%80%E5%90%8E%E7%9A%84%E6%88%BF%E9%97%B4.png)

对于这个房间，我们将为设计添加一些垂直元素。我们还将建造楼梯和电梯进入上面的走道，所以让我们开始：

1.正如我们之前添加的那样，让我们从走廊复制一块地板并将其与门口对齐。这将是我们新房间的开始。这个房间将比最后一个房间大，所以让我们在每个方向复制我们的新楼层两次，创建一排五个楼层。

2.现在让我们通过按住Ctrl并单击每个部分来选择该行中的所有地板块。复制此行四次以创建我们的大房间：

![大房间](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E5%A4%A7%E6%88%BF%E9%97%B4.png)

3. 将走廊的墙壁部分复制到我们的房间，并用它来封闭整个空间，就像我们在走廊里所做的那样。现在选择所有这些墙块并复制它们。将这些碎片放在原件的顶部以创建第二层：

![第二层](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E7%AC%AC%E4%BA%8C%E5%B1%82.png)

4. 现在，让我们为二楼制作catwalk。将地板复制到房间的后面。将其与墙顶对齐。

5. 在Details面板中，转到Scale并在绿色框中键入0.7。这将在Y轴上缩放我们的地板块并减少我们的catwalk的宽度：

![详细信息面板](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E8%AF%A6%E7%BB%86%E4%BF%A1%E6%81%AF%E9%9D%A2%E6%9D%BF.png)

6. 将我们的走道件复制在房间外面，形成一个U形截面。这将为我们的楼梯和电梯留出空间：

![楼梯](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E6%A5%BC%E6%A2%AF.png)

7. 上楼时间！在模式面板的BSP菜单中添加Curved Staircase。将它与我们的角落对齐，以便它与我们的走道连接。但是，默认楼梯不够高。我们可以通过在Details面板中添加楼梯并弄乱Num Steps选项来解决此问题。我们可以通过调整Step Width选项来调整楼梯的大小。对我有用的设置是Num Steps:15和Step Width：275.

8. 我们的最后一个功能是添加我们电梯所需的部件：

![电梯](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E7%94%B5%E6%A2%AF.png)

对于电梯，我复制了一块地板并移动它与我上面的走道对齐。我把它上下移动几次以确保它适合，然后让它坐在地板上的下方位置。我们将动画这一块，让电梯在本章后面工作。

9. 从Architecture文件夹中抓取一个Pillar_50x500件并将它们安排在我们的电梯周围，我们就完成了。

现在我们已经在level中设置了基本level几何体，让我们考虑一下可以添加哪些更多的装饰元素来帮助强化主题。科幻小说有许多不同的风格。某些环境可能干净简洁，例如在星际迷航中。其他人可能更加工业化，到处都是管道和布线，例如我们在Alien特许经营中看到的。水平的美学可用于强化环境的主题并将信息传达给玩家。在这种情况下，我们希望加强生存恐怖方面。要做到这一点，我们更倾向于工业风格。收集参考艺术以帮助激发你的项目放置可以帮助你获得正确的感觉，我强烈建议你在线查看图像以获得一些很好的示例。请记住，这些道具只是可以在以后创建的艺术品的占位符。准备？让我们开始我们的第一个房间：

1.转到Starter Content文件夹中的Shapes文件夹。此文件夹包含许多基本形状，有助于近似可以在Blender中为此级别创建的不同道具。

2.抓住Shape_Cylinder并将其拖入房间。我想象这个第一房间是我们的小型货船的桥梁，并且该圆柱体可以作为用于飞行船的抬头显示器的全息投影仪。我在它上面添加了一个Shape_TriPyramid,并将其缩小了一点，使他看起来更具有技术性。

3.添加几个Shape_Cube片段并将它们缩放为看起来像控制台。这允许我们近似要制作的3D片段的实际尺寸。

4. 使用Shape_Pipe,Shape_Pie_90和Shape_Pipe_180片段，在房间周围添加一些管道以添加更多细节。方形空间中的一个好的经验法则是在角落添加细节以隐藏房间是方形的事实。它使空间更有趣，并提供视觉多样性。

5. 使用Shape_Trim,Shape_Trim_90_In和Shape_Trim_90_out片段，在地板和墙壁相交处添加一些修剪。完成后，选择所有装饰件，复制它们，然后翻转它们以修剪墙壁与天花板相交的区域。

6. Props文件夹包括我们可以使用的几个已完成的部分，与我们将在本书后面使用Blender制作的部分不同。抓住几把椅子，加入我们的桥梁，靠近我们的电脑控制台占位符形状。

7. 再次使用Shape_Cube片段，在背面和侧壁添加一些变化。

这是我完成的这座桥的白盒子：

![桥白盒](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E6%A1%A5%E7%99%BD%E7%9B%92.png)

这是我完成的货舱白盒。

![货仓白盒](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E8%B4%A7%E8%88%B1%E7%99%BD%E7%9B%92.png)

是否开始感觉更像是一个环境？如果没有，请添加更多形状或道具，直到你的水平感觉更自然。但是，不要走得太远。我们希望我们的level能够在其中包含一些对象来传达故事并让玩家沉浸在我们的环境中。我们不希望过度拥挤，让它感到笨拙和混乱。花一些时间在走廊和第二个房间添加一些细节。在下一节中，我们将介绍以我们的主题为基础来阐明我们水平的技巧。

## Using different types of light

在整个level中，我们一直使用基本的灯光来为我们的工作提供一些照明。在本节中，我们将把我们的灯光转换为对我们的主题更加逼真的东西并将其传达给玩家。适当的照明对于场景或环境看起来可信而言非常重要。它可以使观众感到焦虑或害怕，并产生紧张感。它可以传达危险或安全。在游戏中，它甚至可以是游戏机制。在我们的场景中，我们将使用灯光来传达一种神秘感和紧张感，这种紧张感可能会超出玩家的能力范围。

为了创造这种感觉，让我们考虑一下我们可能需要什么。将角落投入阴影并限制玩家的视线可能会让他们认为某些东西可能会跟踪他们，只是看不见。使用不同颜色的灯来表示危险和安全可以将这些事情传达给玩家，从而产生或缓解紧张。就像我们从在线图像中收集灵感来帮助项目放置，来自其他游戏的图像，尤其是现实生活中的图像，可以帮助你找到适合你level的正确造明。虚幻提供了一些不同类型的光来帮助我们实现这些目标。Pointlights是我们熟悉的一种灯。他们从空间的固定点向各个方向投射光线。接下来我们有SpotLights。这些灯将锥形光投射到目标点。这可用于突出显示环境内容。最后，我们有DirectionalLights和SkyLights.这些是大型光源，可在整个level中产生通用光量。DirectionalLights通常用于在室外环境中创建太阳或月亮。对于每种类型的灯光，Details面板提供了几个用于调整强度，阴影，衰减和颜色的选项。准备为我们的环境增添一些情感？

1. 让我们开始我们的造明过程，删除每个房间的一盏灯。这将使我们从一些非常基本的东西开始。在进行照明更改后，不要忘记构建level。这允许Unreal处理阴影的更改，并让你准确地查看更改。

2. 选择位于PlayerStart附近的灯光。我们的小船的桥梁区域是玩家开始的地方，并且应该感觉至少比船的其他部分更安全：

![开始灯光](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E5%BC%80%E5%A7%8B%E7%81%AF%E5%85%89.png)

3. 将灯光的颜色更改为浅绿色。这是通过选择灯光并单击Light Color选项。这将打开一个色轮，允许你为灯光选择新的颜色。

4. 在默认level中，灯光太暗不适合我们的目的。在详细信息面板中，找到Intensity属性并输入较低的值。我将光线设置为250。

5.灯光的效果区域由称为Attenuation的属性控制。这基本上是光从全功率变为零的半径。将Attenuation设置为零的灯根本没有任何衰减，并且处于全强度。我们希望光线不会超过计算机屏幕所能发生的光线。我们把它设置为250.

6. 由于我们希望灯光的亮度与计算机屏幕一样多，因此请将其转移到我们的计算机控制台形状附近。

7.如果我们看一下光线所投射的阴影，它们会非常粗糙和锋利。根本不是我们在现实世界会看到的。大多数照明都会产生非常柔和和漫反射的阴影，我们想在这里模仿它。我们通过在Details面板中添加Source Radius来实现此目的。我们的设定为150：

![灯光设置](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E7%81%AF%E5%85%89%E8%AE%BE%E7%BD%AE.png)

8.现在我们已经完成了灯光的所有设置，让我们将灯光复制到我们的全息显示器（金字塔形状上方）的其他计算机控制台和上方。

9.以下屏幕截图显示了货舱中的最终照明设置：

![灯光最终设置](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E7%81%AF%E5%85%89%E7%9A%84%E6%9C%80%E7%BB%88%E8%AE%BE%E7%BD%AE.png)

确保建立你的level并播放它以检查你的全光桥。一旦你开心，将我们学到的一些技巧应用到走廊和第二个房间，即我们的货舱。请记住，我们正在寻求紧张和神秘。由于这些区域在我们的安全桥梁之外，我喜欢使用红色和黄色光。现在让我们通过使门和楼梯工作，为我们的水平添加一些有趣的互动元素。

## Adding interactive elements using Triggers and Blueprints

现在，我们的游戏水平看起来还不错。我们给了它一些道具，让玩家觉得它们在一艘小型货船内部徘徊。使用灯光，我们向玩家传达了一种危险感和神秘感。完成此级别的最后一步是添加一些基本的交互元素。为此，我们需要一个Blueprint。

Blueprint是虚幻游戏引擎中内置的可视化脚本引擎，允许艺术家和其他非程序员编写游戏机制和level事件，而无需查看一行代码，我在教学期间也发现，这是一种向编程技术介绍自己的好方法，因为Blueprint使用了许多相同的术语。出于我们的目的，我们将使用Blueprint为我们的两扇门和电梯设置动画，以便我们的播放具有一些互动元素：

![蓝图](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E8%93%9D%E5%9B%BE.png)

我们将用作level设计器的大多数基本编程遵循相同的基本模式：事件会导致许多操作发生。例如，为了使门打开，事件可能是玩家走到门口动作是将门设置为打开位置，然后在几秒钟后将其关闭。在构建Blueprint序列时，我们还将学习变量和数据类型。让我们开始我们的门序列：

1. 首先我们需要一个Trigger。这是一个游戏对象，用于检测其他对象（如播放器）是否已进入某个区域。它们有几种不同的形状，几乎可以在任何情况下调整尺寸。在这里，我们将从Modes面板中获取Box Trigger并将其放在我们门的底部。这将导致播放我们动画的事件：

![触发器](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E8%A7%A6%E5%8F%91%E5%99%A8.png)

2. 现在是时候开始我们的序列了。单击Blueprint按钮并选择Open Level Blueprint。通过按住RMB，向一个方向拖动，并使用LMB按钮选择以下内容来导航Blueprint区域：

![蓝图导航](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E8%93%9D%E5%9B%BE%E5%AF%BC%E8%88%AA.png)

3. 返回到level并确保选中了Trigger。现在，在Blueprint窗口中，右键单击空白区域，然后单击Add Event forTigger box 1旁边的向下箭头（你的编号可能不同）。单击Collision旁边的向下箭头，然后选择Add On Actor Begin overlap。当Actor（我们的玩家）开始与Trigger重叠时，此事件触发。

4. 接下来我们需要一个时间轴。这是一个允许你为数值数据类型设置动画的节点，例如float或vector。在我们的例子中，我们将使用它来设置门的矢量位置的动画，使其看起来像是在滑动。右键单击事件旁边的空间，然后转到列表的最底部。选择Add Timeline。你将有机会给它起一个独特的名称。我将我的名字命名为Door1，这不是很具有描述性，但它将与我们创建的任何其他Timeline区分开来。

![时间轴](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E6%97%B6%E9%97%B4%E8%BD%B4.png)

5. 双击节点打开Timeline。由于我们要为矢量（3D空间中的一个点）设置动画，我们需要单击位于Timeline窗口左上角的V+按钮。你将看到三条彩色线条，分别代表X，Y，和Z轴。我们要做的是创建与门的重要位置相对应的关键帧：打开和关闭。在我们添加关键帧之前，我们需要确保我们只是在X轴上工作，因为这是我们将滑动门的方向。我们使用图表左上方Y和Z旁边的小挂锁来完成此操作你可能还想通过单击它们旁边的眼睛来隐藏轴。

6. 在0附近，通过右键单击并选择Add key到X轴。如果你没有完全为零，请随意单击关键帧并将时间和值更改为零。接下来，在2妙时添加另一个键并将其值更改为100.我们告诉门在正X轴方向上滑动100个单位。最后，我们可以通过右键单击第一个键并将Key Interpolation设置为Auto来使滑动变得更逼真。你可以通过单击适合垂直箭头（挂锁附近）查看完整曲线来查看手工。

![蓝图节点](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E8%93%9D%E5%9B%BE%E8%8A%82%E7%82%B9.png)

7.单击其选项卡返回Event Graph。现在我们需要通过让我们的门移动来利用我们的动画值。我们在这里寻找的节点叫做Set Actor Location。在时间轴附近单击鼠标右键，然后在Search框中键入该值。如果在Windows菜单启用了调色板，也可以使用Find a Node库。设置Acotr位置需要两条信息才能工作:目标(正在移动的是什么）和新位置。现在，你可能想要将我们的Timeline右侧的黄色输出连接到新位置，但它不一定有效。我们需要考虑门的现有位置并添加我们的幻灯片。为此我们需要获得我们门的位置。单击关卡中的门，然后右键单击我们的Blueprint。在搜索框中，键入Get Actor Location。我们还需要一个节点调用Vector+Vector来为我们作数学运算。将所有节点连接在一起，就像你在上一张图中看到的那样，通过左键单击并按住输出（例如彩色圆点或箭头),然后拖出导线并插入下一个节点的输入。不要过分担心这部分；Unreal不允许你将节点插入另一个不接受该输入的节点。

8.现在，我们的Get和Set节点仍然缺少某些东西。两个节点都没有目标，因此他们不知道要引用哪个对象。为此，我们需要Name变量。这只是对level中存在的内容的引用。在level中，右键单击我们的Set Actor Location节点旁边的，然后选择Create a Reference to SM_Door2（同样，你的号码可能不同）。现在，将该变量插入到我们节点的目标中。重复此过程为Get Actor Location节点创建名称变量。

9. 该过程的最后一部分是返回level，单击门，然后在Details面板的Transform部分选择Movable。这将允许你的门动画。现在建立关卡并测试它。

10. 一切正常吗？好的！确保再次按照走廊的另一端的第二扇门进行操作。

现在我们已经移动了门，我们将对电梯做同样的事情，只是这次我们将使用稍微不同的过程。Matinee是一个强大的工具，允许动画师和游戏设计师在Unreal内部创建高质量的动画。我们将使用此工具为我们的电梯制作动画：

1. 创建Matinee与创建Timeline略有不同。要启动Matinee，请单击Matinee按钮并选择Add Matinee。Unreal会向你发出一条警告，指出Undo/Redo数据将重置。继续单击继续，这将在你的level中创建一个Matinee对象。不要担心它的位置，这个东西可以在任何地方使用。单击对象，然后在details面板中选择打开Matinee。以下屏幕截图显示了Matinee工具：

![Matinee工具](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/Matinee%E5%B7%A5%E5%85%B7.png)

2. 返回level，单击我们的电梯平台，确保在Details面板中将其设置为Moveable。现在点击Matinee。在Matinee屏幕的Tracks部分，我们将右键单击并从菜单中选择Create New Empty Group.将它命名为独特的东西，例如Elevator。这为我们想要为电梯设置动画的任何对象创建一个组。

3. 接下来，右键单击刚刚创建的组，然后选择Create New Movement Track。这将创建实际的动画轨道，我们可以在其中添加我们的关键帧:

![Matinee界面](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/Matinee%E7%95%8C%E9%9D%A2.png)

4. 当你创建Movement轨迹时，Unreal创建了第一个关键帧为0.这将是我们的向下位置。要为我们的向上位置创建第二个键，请单击Matinee屏幕左上角的Add Key按钮。右键单击该键，然后选择Set Time。在框中输入2，然后按Enter键。在我们的第二把钥匙仍然被选中的情况下，进入level并将我们的电梯移至上升位置。当我们看到创建的虚线从我们的下行位置到新的上升位置时，我们会知道它有效。最后，通过抓住5附近时间栏底部的红色标签并将其拖动到2来更改总Matinee序列的长度。完成后，让我们关闭我们的Matinee：

![完成电梯](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E5%AE%8C%E6%88%90%E7%94%B5%E6%A2%AF.png)

在这一点上，我们需要一些按钮来控制我们的电梯。继续前进到Shapes文件夹，就像我们过去所做的那样，抓住几个我们可以用作调用按钮的形状。我使用了一个金字塔，它已经缩小了一点，以适应平台附近的柱子和墙壁。我们还需要在每个按钮周围添加BoxTriggers，以创建玩家需要使用的激活区域：

![电梯蓝图](https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/3DGameDesignwithUnrealEngine4andBlender/%E7%94%B5%E6%A2%AF%E8%93%9D%E5%9B%BE.png)

6. 在我们的所有按钮和Box Triggers到位后，是时候组装Blueprint序列了。在level中，选择我们将要使用的所有Box触发器。在Blueprint窗口中，右键单击并选择为所选Actor添加事件。这允许你同时为所有触发器框创建On Actor Begin Overlap和On Actor End Overlap。我们还需要搜索输入事件以按E。

7. 我们需要的下一个节点是Gate。这些节点允许你通过序列控制信息流。信息通过Enter输入进入门，并且仅在门打开时才继续。在我们的电梯控制中（见上图），按E键将信息发送到门，但只有当玩家站在其中一个电梯控制按钮时才会打开门。

8. 在Gate节点之后，我们需要一个恰当命名的Flip Flop节点。此节点将执行A或B，具体取决于上次执行的分支。这将允许我们通过播放和倒转我们的Matinee来上下切换电梯。

9. 现在我们要告诉我们的顺序是播放和反转Matinee。在我们的关卡中单击Matinee对象。回到蓝图并右键单击，然后选择创建对我们的Matinee Actor的引用。从Matinee Actor拖出一条线并搜索Play和Reverse节点。将这些添加到Blueprint中。

10. 现在按照你在图像中看到的Blueprint连接，单击编译按钮，然后为该level进行测试！

## Playtesting our level

我们设计的过程的下一步是与朋友，家人以及最重要的是玩游戏的人一起测试我们的原型level。Playtesting是设计过程中最重要和最被忽视的步骤之一。许多游戏和关卡设计师都希望赶紧进行最终设计，并且通过这样做，错过了其他不参与游戏设计和构造的人可以提供的有价值的反馈。重要的是记住，尽管level可能对你来说很有趣，但其他人可能会发现它令人困惑或缺少关键功能。通过允许他们尝试原型获得的反馈可以帮助我们看到我们认为理所当然的事情，因为我们是设计师。

如果这个level是针对商业游戏，我们会花一些时间与朋友和同事一起测试，并在我们去的时候收集反馈。造明可能太暗或按钮太难找到。我们可能会添加更多房间或拼图，以使level更具挑战性。我们甚至可以废弃整个事情重新开始，如果我们受到一致的反馈，人们不理解它在那里的原因。游戏测试需要记住的重要的一点是，玩家的反馈不是对你或你的想法的批评。你从他们那里收集的信息旨在提高你的水平并加强你的设计，所以千万不要错过收集这些重要数据的机会！

## Summary

在本章中，我们基于我们在纸上绘制的设计，使用虚幻引擎4构建了一个关卡。水平本身很简单：两个房间通过走廊连接，门，楼梯和电梯。我们使用Starter Content文件夹中的一系列形状和道具来装饰我们的空间，以适应我们的科幻主题。我们还研究了如何在关卡中使用灯光来创造紧张感并传达情绪。通过Blueprint，我们能通过动画门和电梯来探索level编程。最后，我们讨论了游戏测试的重要性以及我们的玩家的建设性批评如何才能让我们的level和游戏变得更好。在下一章中，我们将开始使用Blender并根据我们在白盒过程中用来装饰船的一些基本形状为我们的level创建道具。

<a href="https://github.com/BlenderCN/blenderTutorial/blob/master/3DGameDesignwithUnrealEngine4andBlender/chapter1.md">
  <img src="https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/blenderpng/logoleft.png" align="left">
</a>
<a href="https://github.com/BlenderCN/blenderTutorial/blob/master/3DGameDesignwithUnrealEngine4andBlender/chapter3.md">
  <img src="https://github.com/BlenderCN/blenderTutorial/blob/master/mDrivEngine/blenderpng/logoright.png" align="right">
</a> 
