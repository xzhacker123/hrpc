# hrpc

Common interface definition based rpc implementation (基于公共接口定义的rpc实现).

```text
+-----------------------------+                                 +------------------------------+
|                             |                                 |                              |
| runtime 1                   |                                 | runtime 2                    |
|                             |                                 |                              |
|                             |                                 |                              |
|                             |                                 |                              |
|                             |                                 |                              |
|                             |                                 |                              |
|                             |                                 |                              |
|                             |                                 |                              |
|       +---------------------+   call remote method            |          +-------------------+
|       | objproxy.methodA()  | +---------------------------->  |          | obj.methodA()     |
|       |                     |                                 |          |                   |
|       |                     |                                 |          |                   |
|       |                     |                                 |          |                   |
+-------+---------^-----------+                                 +----------+---------^---------+
                  |                                                                  |
                  |                                                                  |
                  |                                                                  |
                  +-----------------------------+------------------------------------+
                                                |
                                                |
                                                |
                               +----------------+----------------+
                               |                                 |
                               |  CommonInterface                |
                               |                                 |
                               |                                 |
                               +---------------------------------+
                               |                                 |
                               | + methodA()                     |
                               |                                 |
                               +---------------------------------+
                               |                                 |
                               | + methodB(arg1, arg2)           |
                               |                                 |
                               +---------------------------------+

```