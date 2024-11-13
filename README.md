# Unreal-DS

# Overview

https://dev.epicgames.com/documentation/en-us/unreal-engine/setting-up-dedicated-servers-in-unreal-engine

The server replicates changes from each connected client to simulate the true game state for each connected client. Clients see a close approximation of the game, which is actually being played on the server.

服务器复制来自每个连接的客户端的更改，以模拟每个连接客户端的真实游戏状态。客户端看到的是游戏的近似值，实际上是在服务器上玩的。

# Dedicated Server

A listen server consists of a client hosting the game on their machine and acting as the server. Other clients connect to the hosting client and play the game on the hosting client's instance. In this model, the hosting client is the authoritative host. This gives them an advantage over the connected clients as they are actively playing in the true game state.

监听服务器由一个运行游戏的客户端机器（hosting client，宿主客户端）组成。其他客户端连接到这个客户端，并在这个客户端的实例上玩游戏。在这个模型中， 这给宿主客户端很大优势相对于其他连接的客户端，因为宿主客户端在真正的游戏状态下玩。

A dedicated server consists of a server that runs headlessly. This means that there are no clients playing directly in the dedicated server game instance. Every player comes from a connected, remote client. A headless server does not render any visuals and nobody is playing locally on the headless server.

一个专用服务器由无头运行的服务器组成。这意味着没有客户端直接在专用服务器实例上玩。每个玩家来自连接的远程的客户端。一个无头的服务器不渲染任何视觉并且没有人在无头服务器上玩。

专用服务器比监听服务器有几个优势：

- 更小的容量
- 对宿主客户端没有不公平的优势
- 关注游戏逻辑和客户端提供的信息

监听服务器通常适用于休闲多人游戏和合作游戏，但专用服务器是大型或竞争性游戏的理想选择。