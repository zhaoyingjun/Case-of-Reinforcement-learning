# Case-of-Reinforcement-learning

## 强化学习目前是人工智能领域比较热门的领域，在强化学习领域的框架也是层出不穷。近期国外的一个大神基于TensorFLow2.0开发了一个强化学习框架：huskarl，目前虽然在Github上只有不到400stars，但是我在体验了之后觉得这是一个值得跟进的项目。利用周末的时间，看了一下项目源码，总得来说有如下优点：
1、使用tf2.0的高阶API tf.keras进行编写，具有优秀的可读性
2、实现了与gym的无缝打通，能够直接一行代码引入gym环境。
3、目前实现dqn、ddpg、a2c主流的强化学习算法，可以所用即所得。
4、项目结构非常优化，有利于进行二次开发和定制。
## 总之，我还是非常喜欢这个项目的，我也会在自己业余时间跟进和维护这个项目，希望对强化学习的易用化做点贡献，最最重要的是这个项目是使用TensorFlow2.0写的。[手动狗头]
Talk is cheap,show me the code,所以我也基于这个优秀的huskarl框架使用TensorFlow2.0写了一个强化学习的案例，纯代码在50行以内，但是实现的功能非常的丰富。接下来，就一起看看这个50行代码的案例吧。
# 环境依赖建议：
	Python3.6
	Linux环境（macOSX、Ubuntu以及其他有图形界面的Linux系统）
# 需要安装的依赖：
	pip install huskarl (会自动安装TensorFlow2.0.0alpha版本)
	pip install gym
	pip intsall matplotlib（注意：如果是使用Anaconda创建的虚拟环境，需要使用conda install matplotlib,强烈建议使用Anaconda）
# 代码实现的功能清单：
	检验model_dir文件夹是否存在，并自动创建文件夹
	托扁担（CartPole）游戏环境搭建
	create_model 用于构建Q网络模型，基于tf.keras.Sequential,可以自己试着修改一下网络结构，然后看一下效果。
	rewards 评价反馈图形化展示，可以直观的看到智能体随着训练步数增加获得评价越来越高。
	train用于训练网络模型，每次的训练是在之前训练的基础之上上进行的。
	test用于正式工作，加载模型，将模型处于工作状态，展示模型的工作效果。
效果展示：
如果是使用Anaconda创建的环境，则需要使用pythonw 来执行代码文件，如 pythonw dqn.py。
效果1：

 

效果2：训练状态

 


效果3：工作状态
 
