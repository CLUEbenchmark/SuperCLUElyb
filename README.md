# SuperCLUE琅琊榜
SuperCLUE琅琊榜：中文通用大模型匿名对战评价基准

我们展示了SuperCLUE琅琊榜，这是一个中文通用大模型对战评价基准，它以众包的方式提供匿名、随机的对战。在本文中，我们发布了初步的结果和基于Elo评级
系统的排行榜，Elo评级是国际象棋和其他竞技游戏中广泛使用的评级系统。我们邀请整个社区加入这项工作，贡献新的模型，并通过提问和投票选出你最喜欢的答案来评估它们。


- [介绍Introduction](#介绍Introduction)
- [数据搜集DataCollection](#数据收集DataCollection)
- [两两对战盈率](#两两对战盈率)
- [中文模型初步评价](#中文模型初步评价)
- [Elo评分系统](#Elo评分系统)
- [后续计划](#后续计划)
- [加入我们](#加入我们)
- [链接](#链接)


<img src="https://github.com/CLUEbenchmark/SuperCLUELYB/blob/master/resources/img/supercluelyb_rank.png"  width="100%" height="100%"></img>

   表格1：基于5.8K投票数据，使用Elo机制获得的16个模型的排名。你可以在<a href='https://www.superclueai.com'>琅琊榜</a>上查看

<img src="https://github.com/CLUEbenchmark/SuperCLUELYB/blob/master/resources/img/battle.png"  width="100%" height="100%"></img>
    
    图片1：一对一的投票



## 介绍Introduction

    这里写为什么做这个，有什么问题，好的系统需要的特性，然后是我们的工作。
    
    ChatGPT的巨大成功之后，国内外大量的通用大模被微调用于遵循指令。这些模型能够在回答用户的问题/提示时提供有价值的帮助。
    典型的模型包括ChatGLM,MOSS,RWKV,基于基于LLaMA的Vicua,BELLE等。
    
    尽管每周都会不断发布新的模型，但社区对这些模型的基准测评缺面临着一些挑战，特别是开放式问题的测试。
    好的基准系统，需要有可扩展性，即可以支持大量的模型；可以对新增的模型进行快速的测试。该系统具备这样的特性。
    当前的一些中文通用大基准测试，多基于学术与专业能力测试，虽然可以考察模型的专业能力，但并没有直接针对开放式问题的测试；
    也可能不是针对生成式问题效果的直接测试，如考察模型在这个能力上理解层面的测试。
    
    这里我们介绍了SuperCLUE琅琊榜，这是一个中文通用模型基准平台，以众包方式提供匿名随机对战。聊天机器人竞技场采用Elo评级系统，
    这是国际象棋和其他竞技游戏中广泛使用的评级系统。
    
    为了收集数据，我们在5月19日推出了几个流行的可用于中文通用模型，包括开源模型。在琅琊榜，用户可以与两个匿名模型进行交互，
    并投票选出哪一个更好。


<img src="https://github.com/CLUEbenchmark/SuperCLUELYB/blob/master/resources/img/benchmarks.png"  width="100%" height="100%"></img>


## 数据搜集DataCollection
   
    这里写数据收集过程，结果，初步的一两个统计信息
    
    可以在www.SuperCLUEAI.com使用我系统。当用户进入竞技场时，他们可以并排与两个匿名模型聊天，如图1所示。一旦提交投票，模型名称将被公布。
    用户可以继续用两个新的随机选择的匿名模型重新开始一场新的对战。该平台记录所有用户交互。在我们的分析中，我们只在模型名称隐藏时使用投票。
    琅琊榜在5月19日启动，从那时起，我们已经收集了5.8k张有效的匿名选票。我们在这里做一个简短的总结。
     
<img src="https://github.com/CLUEbenchmark/SuperCLUELYB/blob/master/resources/img/battle_count.png"  width="100%" height="100%"></img>
图片2：每种模型组合的对战次数。模型的匹配，总体上根据采用具有随机性；同时我们也将模型进行了分组，组内的模型具有比随机更高的对战机会。

## 两两对战盈率
        
     作为校准的基础，我们在这里还展示了对战中每个模型的成对获胜率。
   <img src="https://github.com/CLUEbenchmark/SuperCLUELYB/blob/master/resources/img/battle_winrate.png"  width="100%" height="100%"></img>
图: 模型A在所有非平局的A对B战斗中获胜的分数。

   
## 中文模型初步评价

    TODO 

## Elo评分系统
   
    介绍一下Elo的原理
    
    Elo评分系统是一种计算参赛者相对技能水平的方法，在竞技游戏和体育运动中被广泛采用。两名参赛者之间的评分差异可以作为比赛结果的预测因素。
    Elo评级系统适用于我们的案例，因为我们有多个模型，并且我们在它们之间进行对战。如果玩家A的评分为Ra，玩家B的评分为Rb，
    则玩家A获胜概率的确切公式为：
    

   <img src="https://github.com/CLUEbenchmark/SuperCLUELYB/blob/master/resources/img/elo_gongshi.png"  width="80%" height="80%"></img>
   
   玩家的评分可以在每次战斗后线性更新。

## 后续计划
    
    新增一些模型，定时更新（每月），加入task type；
    公布投票数据（有限），数据分析情况

## 加入我们
    
     邀请社区来使用，包括链接

## 链接
     
     网站，排行榜，Github项目，colab notebook待添加