# cmpe260-project-1-solved
**TO GET THIS SOLUTION VISIT:** [CMPE260 Project 1 Solved](https://www.ankitcodinghub.com/product/cmpe260-project-1-solved-2/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;93963&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CMPE260 Project 1 Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
1 Introduction

In this project, you will write a logic for an agent to do several tasks in a very tiny version of Minecraft.

2 Knowledge Base

We have already implemented the mechanics of the game for you in cmpecraft.pro and constants.pro. You should not modify these files. The map for the game is given in map.txt. You can change it to test your agent in different settings.

The main data structure for this project is given in state/3 predicate. After you load your main file (main.pro), you can check the current state with the following query:

?- state(AgentDict, ObjectDict, Time).

AgentDict = agent dict{hp:10, hunger:100000, inventory:bag{}, x:3, y:4},

ObjectDict = object dict{0:object{hp:3, type:stone, x:2, y:1}, …}

Time = 1

########## # S TT S# # O TT C# # TT# #@ C# #C S# ##########

This state is generated from the map file map.txt. Here, each character represents a different object in the game: • #: Walls and bedrocks.

• @: The agent.

• S: Stone.

• T: Tree.

• O: Food.

• C: Cobblestone.

The agent dictionary consists of four attributes: hp (hit points), hunger (hunger level), x (x-axis location), y (y-axis location), and inventory. The agent can collect different items from different objects, and store them in its inventory. The inventory is a dictionary that contains the name of the item as the key, and the number of that item as the value.

The object dictionary holds objects in the environment. Each item in this dictionary is also represented as a dictionary which has four attributes: hp (how many left clicks are required to mine this object), type, x, y.

Each object yields an item when they are mined, or chopped, or collected. Namely, if the agent mines a stone (i.e. left clicks to the tile that contain a stone until the stone’s hp drops below zero), the stone yields three cobblestones. This information is provided in yields/2 in constants.pro.

The agent has (is going to have) four main actions: place a cobblestone, left clicking in a specific direction, crafting items, and moving in a direction. These low-level actions are provided for you. In other words, given an

</div>
</div>
<div class="layoutArea">
<div class="column">
1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
environment state, you can find the next state after executing one of these actions. You can execute random move. to see the agent executing random actions.

3 Predicates

In this section, we will go over the predicates that you are going to implement.

3.1 manhattan distance(+List1, +List2, -Distance) 10 points

This predicate will compute the Manhattan distance between two lists that contain two items each. The Manhattan

distance is the fancy name for l1 norm:

D([x1, y1], [x2, y2]) = |x1 − x2| + |y1 − y2| (1)

All test cases will contain valid List1 and List2 (i.e. no empty lists). Examples:

?- manhattan distance([1, 2], [3, 7], D). D = 7.

?- manhattan distance([12, 3], [3, 7], D). D = 13.

3.2 minimum of list(+List, -Minimum) 10 points

This predicate will unify Minimum with the minimum of List. All test cases will contain valid List (i.e. no empty

lists).

Examples:

?- minimum of list([3, 7, 1, 4], M). M = 1.

?- minimum of list([34], M).

M = 34.

3.3 find nearest type(+State, +ObjectType, -ObjKey, -Object, -Distance) 10 points

This predicate will find the closest ObjectType in the given State, and unify the found object’s key (in the ObjectDict) with ObjKey, unify the found object with Object, and unify the Manhattan distance between the object and the agent with Distance. Here, State is a list: [AgentDict, ObjectDict, Time]. If there is no object with the given type, the predicate should be false. The following examples are valid for the given example map file.

Examples:

?- state(A, O, T), State=[A, O, T], find nearest type(State, tree, Key, Obj, Dist). K = 5,

Obj = object{hp:3, type:tree, x:4, y:2},

Dist = 3.

?- state(A, O, T), State=[A, O, T], find nearest type(State, stone, Key, Obj, Dist). K = 0,

Obj = object{hp:3, type:tree, x:2, y:1},

Dist = 4.

3.4 navigate to(+State, +X, +Y, -ActionList, +DepthLimit) 10 points

This predicate will give an ActionList that will navigate the agent to X and Y location. The number of actions in ActionList should not be greater than DepthLimit, though, it can be less than the depth limit1. All test cases will contain valid X and Y. The following examples are valid for the given example map file.

1If you do not introduce such a depth limit, you might stuck into an infinite loop, depending on your implementation 2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
Examples:

</div>
</div>
<div class="layoutArea">
<div class="column">
?- state(A, O, T), State=[A, O, T], navigate to(State, 6, 5, ActionList, 3). false.

?- state(A, O, T), State=[A, O, T], navigate to(State, 6, 5, ActionList, 4). ActionList = [go right, go right, go right, go down]

?- state(A, O, T), State=[A, O, T], navigate to(State, 6, 5, ActionList, 5). ActionList = [go right, go right, go right, go down]

3.5 chop nearest tree(+State, -ActionList) 10 points

This predicate will generate the necessary actions to find the nearest tree, navigate to that location, and chop it (i.e. left clicking to it four times). After executing the action list, the agent should have the yield of the tree in its inventory. If there is no tree in the state, then the predicate should be false. The following example is valid for the given example map file.

Examples:

?- state(A, O, T), State=[A, O, T], chop nearest tree(State, ActionList).

ActionList = [go right, go up, go up, left click c, left click c, left click c, left click c]

3.6 mine nearest stone(+State, -ActionList) 10 points

This predicate will generate the necessary actions to find the nearest stone, navigate to that location, and mine it (i.e. left clicking to it four times). After executing the action list, the agent should have the yield of the stone in its inventory. If there is no mine in the state, then the predicate should be false. The following example is valid for the given example map file.

Examples:

?- state(A, O, T), State=[A, O, T], chop nearest tree(State, ActionList).

ActionList = [go up, go up, go up, go left, left click c, left click c, left click c, left click c]

3.7 gather nearest food(+State, -ActionList) 10 points

This predicate will generate the necessary actions to find the nearest food resource, navigate to that location, and collect it (i.e. left clicking to it one time). After executing the action list, the agent should have the yield of the food in its inventory. If there is no food in the state, then the predicate should be false. The following example is valid for the given example map file.

Examples:

?- state(A, O, T), State=[A, O, T], gather nearest food(State, ActionList). ActionList = [go up, go up, go left, left click c]

3.8 collect requirements(+State, +ItemType, -ActionList) 10 points

Given an item type, for example stone pickaxe, this predicate will generate the necessary actions to collect the required items to craft a stone pickaxe. After executing the action list, the agent should be able to craft a stone pickaxe. If the current map does not contain all the requirements, then the predicate should be false. The following example is valid for the given example map file.

Examples:

?- state(A, O, T), State=[A, O, T], gather nearest food(State, ActionList). ActionList = [go right, go up, go up, left click c | …]

</div>
</div>
<div class="layoutArea">
<div class="column">
3

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
3.9 find castle location(+State, -XMin, -YMin, -XMax, -YMax) 5 points

This predicate will help the agent to find a location to build a castle. Castle is just a fancy name for a three by three cobblestone blocks. An appropriate location for a castle is a three by three area that does not contain any object. If there is no appropriate location, then the predicate should be false. The following example is valid for the given example map file.

Examples:

?- state(A, O, T), State=[A, O, T], find castle location(State, XMin, YMin, XMax, YMax). XMin = 2,YMin = 3,XMax = 4,YMax = 5.

3.10 make castle(+State, -ActionList) 15 points

This predicate will generate an action list to first acquire the necessary requirements for building a castle (i.e. nine cobblestones, so the agent should first mine three stone blocks), then find a castle location, then build the castle by placing cobblestone tiles into a three by three area. If there is no appropriate location or resources, then the predicate should be false. The following example is valid for the given example map file.

Examples:

?- state(A, O, T), State=[A, O, T], make castle(State, ActionList). ActionList = [go up, go up, go up, go left, left click c | …].

3.11 Printing states

You can use execute actions/3 and execute print actions/3 (same as execute actions) but renders the game state in ASCII) which simulates the action list from the given state and return the final state. For example, ?- state(A, O, T), State=[A, O, T], make castle(State, ActionList),

execute print actions(State, ActionList, FinalState).

This will help you see the actions of the agent, and hopefully allow you to debug more easily.

4 Documentation

Please explain what each predicate is for with comments in the code. Codes with no comments might lose points if a predicate is too hard to understand.

</div>
</div>
</div>
