# NeedToReview
1. 浮点数【**下溢**】直接当作”0“处理，浮点数【**上溢**】产生中断或异常，处理上溢错误。

2. 分区分配内存管理：类似下图。采用【**界地址保护**】来保护不同的分区。

   ![25F5CF98-05FE-4843-8655-456DC8D77DC0](/Users/cncaoyue/Library/Containers/com.tencent.qq/Data/Library/Application Support/QQ/Users/304960005/QQ/Temp.db/25F5CF98-05FE-4843-8655-456DC8D77DC0.png)

   

   

   3. 建立符号链接（软链接）时，引用计数值【直接复制】；建立硬链接时，【引用计数值+1】。删除文件时，删除操作对于符号链接（软链接）是不可见的，当下一次访问时才会发现文件已被删除，直接删除符号链接（软链接）；但是对于硬链接，删除文件，引用计数值-1，当引用计数值为0时，再删除。

   4. 端到端和点到点。

      OSI参考模型中，自下而上第一个提供端到端服务的层次是【传输层】。

      端到端是：

      ![image-20201125190238952](/Users/cncaoyue/Library/Application Support/typora-user-images/image-20201125190238952.png)

      

      点到点是：

      OSI参考模型中，提供点到点服务的是数据链路层和网络层。

      ![image-20201125190342481](/Users/cncaoyue/Library/Application Support/typora-user-images/image-20201125190342481.png)

   5. CSMA/CD协议的网络中，最小数据帧长度减少，那么争用期就要变短。争用期是就是2t，是往返时延。数据帧减小，那么也就是争用期要变短，不然的话察觉不到冲突就被发出去了。争用期变短是通过减小往返时延实现的，也就是减小站点之间的距离。

   6. FTP客户和服务器之间传递FTP命令时，使用的连接是建立在TCP之上的控制连接。

   7. 假定用若干个2k * 4位的芯片组成一个8k * 8位的存储器，则地址0B1FH所在芯片的最小地址是：？

      首先看该8k * 8位存储器的组成：

      ![616EF6B5E8C0F7DA609B7CC6ECB5B711](/Users/cncaoyue/Desktop/616EF6B5E8C0F7DA609B7CC6ECB5B711.jpg)

      
   
      则0B1FH在第2块，最低地址为0800H。
   
      8. 进程互斥访问，这个需要找几个题，找几个代码来看看才可以。干说我也说不上来。
      
      9. RIP协议的坏消息传播慢怎么理解？
      
         答：RIP中的消息每隔30秒发送一次，只给相邻节点。当图中R1发现C不可达时，将自己的路由表改成16，并且准备在下一个30秒告诉R2，但是R2现在就会告诉R1，R2到C的跳数是2，于是R1到C的跳数就会变成3。现在R1路由表中到C已经变成3了，然后R1和R2再不断更新信息，过程是：
      
         R2改成4，R1改成5，R2改成6，R1改成7。。。直到都变成16，才发现原来C已经不可达了。这就是坏消息传播慢的原因。

![这里写图片描述](https://img-blog.csdn.net/20161220215141074?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvdTAxMTI0MDAxNg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

10. 路由器可以抑制广播风暴。另外：

    |        | 是否隔离冲突域 | 是否隔离广播域 |
    | ------ | -------------- | -------------- |
    | 集线器 | 0              | 0              |
    | 网桥   | 1              | 0              |
    | 交换机 | 1              | 0              |
    | 路由器 | 1              | 1              |

11. 回路对应路径，简单回路对应简单路径。

12. hash表的装载因子就是【表内元素数/表长】。

13. 相对寻址：一定是PC的寻址才叫相对寻址。基址寻址和变址寻址区分开。

14. 系统总线的数据线传输【指令、操作数、中断类型号等】，握手（应答）信号在通信总线上传输。

15. 【响应比=（作业执行时间+作业等待时间）/作业执行时间】。

16. I/O系统从上到下的层级结构是：（其中与设备无关软件层可以指【系统调用】）

    ![A5279F1A-5BCB-468B-9A80-4E631312DDC3](/Users/cncaoyue/Library/Containers/com.tencent.qq/Data/Library/Application Support/QQ/Users/304960005/QQ/Temp.db/A5279F1A-5BCB-468B-9A80-4E631312DDC3.png)

17. 在虚拟内存管理中，地址变换机构将逻辑地址变换为物理地址，形成该逻辑地址的阶段是【编译】。

18. TCP/IP参考模型的网络层提供的是【无连接不可靠的数据报服务】。

19. CSMA/CA（Carrier Sense Multiple Access with Collision Avoid），通常用于无线局域网。利用ACK信号来避免冲突的发生，只有当客户端收到网络上返回的ACK信号才确认发送出去的消息正确到达。

20. 平衡二叉树的结点平衡因子是【左子树高度 - 右子树高度】。

21. 闪存【Flash Memory】中信息可读可写，但是读取速度一般比写入速度快数倍。存储元由MOS管组成，是一种半导体存储器。

22. 微指令中操作控制字段有两种，一种是字段直接编码法【类似指令】，且微命令需要按互斥分类。另一种是直接编码法【类似位图】。

23. 级联指把两个及以上的设备通过某种方式连接起来。

24. I/O接口命令字和地址线都是单向从CPU传到I/O接口的（这是肯定的啊）。

25. 在进程处于临界区时也可能可以进行处理机调度（临界区是打印机等）。

26. 比特数为k，则窗口大小为【2<sup>k</sup> - 1】，还要留一个用来区分新旧轮次。

27. SMTP是推，POP3是拉。

28. 海明码若能纠一位错，则【2<sup>k</sup> >= n + k + 1】，其中k是校验位数，n是数据位数。

29.  *AGP*（Accelerated Graphics Port）是在PCI总线基础上发展起来的，主要针对图形显示方面进行优化，专门用于图形显示卡。

30. RAID条带化就是类似低位交叉的东西。

31. 银行家算法可以避免死锁。

32. 安全状态一定没有死锁进程。

33. 10base-T采用曼彻斯特编码。

34. 以太网交换机直通交换方式是指以太网交换机可以在各端口间交换数据。它在输入端口检测到一个数据包时，检查该包的包头，获取该包的目的地址，启动内部的动态查找表转换成相应的输出端口，在输入与输出交叉处接通，把数据包直通到相应的端口，实现交换的功能。通常情况下，直通交换方式只检查数据包的包头即前14个字节，由于不需要考虑签到码，只需要检测目的地址的6B，所以最短传输时延是0.48us（100Mbps交换机）。

35. SMTP只支持ASCII码传输。支持在邮件服务器之间发送邮件（废话），支持从用户代理向邮件服务器发送邮件。

36. DRAM是地址线复用技术。

37. 采用指令cache和数据cache分离的主要目的是【减少指令流水线资源冲突】。

38. 微程序控制器中确定下条微指令地址有【计数器法】和【断定法】，其中【计数器法】类似于PC的自动+1，【断定法】类似PC的跳转指令，其下条地址是在微指令中的下址字段给出的。

39. I/O接口中状态端口和控制端口可以合用同一个寄存器。

40. cache的结构如下：

    ![638DCB07-0B2A-4B39-92D9-95B6C34CA43B](/Users/cncaoyue/Library/Containers/com.tencent.qq/Data/Library/Application Support/QQ/Users/304960005/QQ/Temp.db/638DCB07-0B2A-4B39-92D9-95B6C34CA43B.png)

    cache里面是只有Address的前面的tag的，后面的set index和block offset都是没有的。。。因为set index是用来选行的，block offset没啥用，cache是直接读一整个块。还是要看清cache结构。
    
41. DRAM和SDRAM都需要周期性刷新。并且DRAM还是地址线复用。【SDRAM不清楚需不需要地址线复用】

42. 银行家算法不会限制用户申请资源的顺序，仅仅是限制操作系统分配资源的顺序。注意，不要把这两点搞混淆了。

43. 页面分配策略有【可变分配（页面数目可以变多）、固定分配（页面数目固定）】，页面置换策略有【全局置换（有一个空闲队列用来维护空闲的物理快）、局部置换（没有空闲队列）】。

44. POP3使用的是【有连接可靠的数据传输服务】。

45. 以太网交换机本质上是一种多端口的网桥。

46. ```c++
    for(k=0;k<1000;k++)
    {
    		a[k] = a[k] + 32;
    }
    ```

    该代码段中，a[k] = a[k] + 32，需要访问内存两次【读一次，写一次】。

47. 单周期处理器在指令执行过程中控制信号不变，如下图：

    ![img](https://pic4.zhimg.com/80/v2-aebf8f87071c434c2420c9d3e2cdda4c_720w.jpg?source=1940ef5c)

    控制信号确实是不变的。

48. 分离事物通信方式可以提高总线利用率。【虽然我不知道分离事物通信方式是什么意思，百度上需要9.9元才能查看，我也懒得花钱，但是顾名思义，应该就是分离，这个明显可以提高总线利用率】。

49. 缺页是异常。存储保护错也是异常。

50. 批处理系统的多个用户【不能】与计算机直接交互，批处理是多个用户提交作业，等处理器处理完了之后再返回，故不能直接交互。

51. TSL（test and set lock）是采用硬件方式实现的。

52. SPOOLing技术由【操作系统】控制设备与输入/输出井之间的数据传送。

53. 管程就是编程语言中的class。

54. 指令流水线数据通路不包含生成控制信号的控制部件。【上次写的MIPS，控制信号都是外面的bench发出的。】

55. PCIE是串行传输。

56. I/O指令实现的数据传输通常发生在【通用寄存器和I/O端口之间】，（肯定是啊，平时写的汇编不都是这样的吗。。。）。

57. 硬盘读写基本单位：扇区。系统分配磁盘空间的基本单位：簇。

58. ![700D58AC-8632-44A5-AA45-2E43AC131D7C](/Users/cncaoyue/Library/Containers/com.tencent.qq/Data/Library/Application Support/QQ/Users/304960005/QQ/Temp.db/700D58AC-8632-44A5-AA45-2E43AC131D7C.png)

59. 系统将数据从磁盘读到内存的过程中包括：

    （1）初始化DMA控制器并启动磁盘。

    （2）从磁盘传输一块数据到内存缓冲区。

    （3）DMA控制器发出中断请求。（传输完毕）

    （4）执行“DMA结束”中断服务程序。

60. IEEE 802.11数据帧的地址1是【接收站地址】，地址2是【源地址】，地址3是【目的地址】。

61. 直接封装RIP的协议是【UDP】，OSPF的协议是【IP】，BGP的协议是【TCP】。

62. x是管程内的条件变量，则执行x.wait()时，阻塞该进程，并将之插入x的阻塞队列中。

63. 信号量方法可以实现让权等待。

64. 传输层无连接服务的是DNS。

65. IEEE 802.11无线局域网的MAC协议CSMA/CA进行信道预约的方法是【交换RTS与CTS帧】。

66. 信道利用率是与时间相关的量，其计算公式是【发送数据消耗的时间/（发送数据消耗的时间+往返时延）】。

67. IP分组分片的长度必须是8B的整数倍。而且IP分组偏移量也是按8B进行偏移的（意思就是，若MTU=800B，对1500B的IP分组进行分片，应该分成两片，且第一片的分组长度是（（800-20）/8）（下取整） * 8）=776B，第一个分组的片偏移是0，第二个分组的片偏移是776/8 = 97（按8B一组进行偏移）。
