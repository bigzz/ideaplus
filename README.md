# ideaPlus

#### 内存碎片化检测工具

Android 最近跑 monkey 老报内存碎片化严重导致 android 重启的问题，而当前的状况是，无论上层底层都没有一个好的办法来定位问题，所谓的问题就是什么原因导致了碎片化如此严重。

所以，我的想法很简单，在userspace写一个工具不断读取内核的碎片化程度接口，然后当碎片化持续达到某一程度后就dump一些信息并保存到sdcard。

例如进程/线程的内存信息，ION的debug信息等。


#### CPU Hotplug 统一化

每家平台厂商都会推出自己的一套hotplug算法，但是性能／功耗各自参差不齐，是否可以集各家所长，实现一套统一的hotplug算法，只需要去匹配各芯片开关核特性即可？

