1. 静态构造函数
   - 这是个问题？
2. 私有构造函数
   - 只能通过静态方法创建实例。
3. 私有析构函数
   - 无法在栈上创建，可在堆上创建，直接delete会出错，需要在成员函数中使用delete this释放内存。
4. 函数指针
   - typedef int(* test_func)(int , int)：test_func为函数指针类型。
   - int(* test_func)(int, int)：test_func为函数指针变量。
5. 匿名函数
   - [\](int a\){return a;};
6. C++ 模板template和template有区别吗？
   - template\<class A\>和template\<typename A\>没有区别。
7. 如何理解C++左右值？
   - L-value中的L指的是Location，表示可寻址。A value (computer science)that has an address.
   - R-value中的R指的是Read，表示可读。in computer science, a value that does not have an address in a computer language
   - 左右值易错题型：
     - int a=5则++(a++)的值是：编译出错
       - ++是一目运算符，自增运算，它只能作用于一个变量，++（a++）中a++优先，是表达式，不能对表达式进行前加运算
8. 指针常量与常量指针的区别
   - const int *：常量指针，int * const：指针常量
9. __thread关键字
10. 空指针、野指针、悬挂指针（迷途指针）
   - 空指针：指向NULL或nullptr，NULL与nullptr不一样(有哪些不一样？)。
   - 野指针：未被初始化的指针。
   - 悬挂指针（迷途指针）：指针指向的对象已经被delete。
11. NULL与nullptr的区别
12. c++中的锁机制
    - 锁的类型
      - 互斥锁：互斥锁维护一个等待队列，锁被释放后从队列中调度线程，不浪费cpu。
      - 条件锁(条件变量)：条件变量解决了线程等待执行的问题。条件变量能够实现指定条件下唤起线程，避免了频繁的加锁和解锁。
      - 自旋锁：如果无法获取资源，则一直尝试获取资源，浪费cpu。
      - 读写锁：读操作不需要加锁，写操作加锁。
13. typedef是如何实现的
14. IO多路复用epoll的实现机制
15. static、extern、const关键字
16. void *的含义
    - void *指向任何类型的指针。
17. STL容器实现原理
    - unordered_map
    - vector
    - deque
    - map
18. 堆的相关接口

