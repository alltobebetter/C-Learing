# 使用 * 号输出字母 C

**题目：** 使用 `*` 号字符输出字母 C 的图案。

**程序分析：**  将字母 C 的图案分解成多行，每行使用 `printf` 函数输出相应的 `*` 号和空格。

**实例 1： 直接使用 `printf` 输出**

```c
#include "stdio.h"

int main() {
    printf("用 * 号输出字母 C!\n");
    printf(" ****\n");
    printf(" *\n");
    printf(" * \n"); 
    printf(" ****\n");
    return 0;
}
```

**实例 2： 使用字符串数组存储图案**

```c
#include <stdio.h>

int main() {
    // 使用字符串数组存储字母 C 的图案
    const char *c_pattern[] = {
        " ****",
        " *",
        " *",
        " ****"
    };

    printf("用 * 号输出字母 C!\n");
    // 使用循环遍历字符串数组，逐行输出图案
    for (int i = 0; i < sizeof(c_pattern) / sizeof(c_pattern[0]); i++) {
        printf("%s\n", c_pattern[i]); 
    }

    return 0;
}
```

**总结：**

*   **实例 1** 使用最直观的 `printf` 函数直接输出字母 C 的图案，代码简单易懂，但可扩展性较差。
*   **实例 2** 将字母 C 的图案存储在字符串数组中，并使用循环输出，代码更加灵活，易于修改和扩展。例如，可以通过修改 `c_pattern` 数组的内容来输出不同大小或样式的字母 C。

推荐使用**实例 2** 的方式，将图案数据与输出逻辑分离，可以提高代码的可读性和可维护性。
