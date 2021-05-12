# 总结一下面试题
## Q：面向对象的语言特性？
A：封装性、继承性、多态性。

## Q：WebApi中常见的过滤器
A：Authorization、Action、Exception

## Q：手写一个冒泡排序
A：
``` c#
public static void BubbleSort()
{
    bool hasEx = false;
    int[] array = new int[] { 50, 1, 3, 20, 15, 12, 2 };
    for (int i = 0; i < array.Length; i++)
    {
        for (int j = array.Length - 1; j > i; j--)
        {
            if (array[j] < array[j - 1])
            {
                Exchange(ref array[j], ref array[j - 1]);
                hasEx = true;
            }
        }
        if (!hasEx)
        {
            return;
        }
    }
    foreach (var item in array)
    {
        Console.WriteLine(item);
    }
}

private static void Exchange(ref int x, ref int y)
{
    int temp = x;
    x = y;
    y = temp;
}

```

## Q：手写一个递归
A：
``` c#
public class MainClass
{
    public static void Main() { Console.WriteLine(Foo(30)); }
    public static int Foo(int i)
    {
        if (i <= 0) return 0;
        else if (i > 0 && i <= 2) return 1;
        else return Foo(i - 1) + Foo(i - 2);
    }
}
```

## Q：overload 和 override 的区别
A：
 > overload：指在一个类中的方法与另一个方法同名，但是参数列表不同 <br>
   override：当一个子类继承一个父类，子类中的方法名称、参数列表和父类完全相同 

