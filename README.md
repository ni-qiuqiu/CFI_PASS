# CFI_PASS
Android kernel  cfi pass

关于5系加载lkm会panic的问题 

经过测试在gki源码树中整编driver编译出来的模块不会有问题（也是目前内核root的编译方式），而在out-of-tree中就存在cfi检查失败

此模块就是用来pass掉cfi check（思路来自skroot），加载cfi模块后（可以直接卸载，重启后失效），是直接ret了cfi check（慎用）
