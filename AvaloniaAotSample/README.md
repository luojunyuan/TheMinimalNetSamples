create by template `Avalonia .Net App (AvaloniaUI)`

| AOT build |  |
| --- | --- |
| When launch | 76.1 MB |
| Leave it along | 76.3 MB | 
| Switch fullscreen | 113.2 MB | 
| A small window | 47.3 MB | 
| A normal window | 62.8 MB | 
| After long time | 64.5 MB | 


普通编译 在 arm-win 上400*300小窗口静止后 23mb。。aot后更小的窗口还能低到16mb 20mb，可能是arm的特性

BaseBlankMem 空窗口的固定内存开销 18.87MB
PerMillionPixel 每百万像素约增加 13.4MB 的内存占用

内存占用（MB） ≈ BaseBlankMem + PerMillionPixel × 像素数（百万）

比如现在PD虚拟机内全屏 1512*874.5*2^2(dpi) / 1,000,000 * PerMillionPixel + BaseBlankMem = 89.7422784
实际任务管理器是 89.9MB 完全一致
