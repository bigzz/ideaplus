# ideaPlus

#### 内存碎片化检测工具

Android 最近跑 monkey 老报内存碎片化严重导致 android 重启的问题，而当前的状况是，无论上层底层都没有一个好的办法来定位问题，所谓的问题就是什么原因导致了碎片化如此严重。

所以，我的想法很简单，在userspace写一个工具不断读取内核的碎片化程度接口，然后当碎片化持续达到某一程度后就dump一些信息并保存到sdcard。

例如进程/线程的内存信息，ION的debug信息等。


#### CPU Hotplug 统一化

每家平台厂商都会推出自己的一套hotplug算法，但是性能／功耗各自参差不齐，是否可以集各家所长，实现一套统一的hotplug算法，只需要去匹配各芯片开关核特性即可？


#### gpufreq是否可以与cpufreq 互相平衡？
可能有一种情形：例如nba2k14,在投篮后篮球与篮框接触的瞬间，可能需要大量的碰撞检测等计算，这部分可能把loading转嫁到cpu了，而gpu的loading一下子降低到了极低，因而gpufreq会降低到很低的水平；而等cpu计算完成后，gpu又不能快速将gpufreq拉起来，导致游戏卡顿。


#### Hotplug后migration加速?
hotplug后cpu的频率处于一个较低的状态，是否需要锁定来提高migration的效率？


#### CPU Freq/CPU Hotpulg 参数 Tunning 工具

实现一个apk 和 某个同平台的配置文件，给到测试组同时根据特定的场景tunning 一组合适的参数用于基本配置数据，然后进行功耗测试。


#### Perf Event 结合systrace前端
整合systrace与perf event，协助分析性能问题。


#### 如何绕过r7 plus不能进入fastboot的问题？

#### cm构建代码的方法
vendor部分从手机提取。


#### m86 merge with cm

#### BSP阶段借助Top 50 游戏来tunning cpu/gpu/mem 参数。