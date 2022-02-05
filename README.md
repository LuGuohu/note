Executors -- new ThreadPoolExecutor

ThreadPoolExecutor extends AbstractExecutorService

AbstractExecutorService(抽象类) implements ExecutorService

interface ExecutorService extends Executor

什么是线程池
为了避免重复的创建线程 线程池的出现可以让线程复用 通俗的讲 当有任务来的时候 就会像线程池里面拿一个线程 当工作完成后 不是关闭线程 而是归还线程到线程池中

这样避免了重复开销 这样就会节省性能和时间

线程池的核心讲解
核心参数

corePoolsize : 线程中允许的核心线程数

maximumPoolsize : 该线程所允许的最大线程数

keepAliveTime : 空余线程的存活时间并不会对所有的线程起作用 如果线程数大于corePoolsize 那么这些线程就不会因为被空闲太久而关闭 除非你调用 allowcorethreadtimeout 方法 这个方法可以使核心线程数也被回收

只有当线程池中的线程数大于corePoolSize时keepAliveTime才会起作用,知道线程中的线程数不大于corepoolSIze,
unit : 时间单位

workQueue : 阻塞队列 在此的作用就是用来存放线程

threadFatory: 线程工厂 可以为线程池创建新线程

defaultHnadler: 拒绝策略 当线程失败等 如何处理方式
