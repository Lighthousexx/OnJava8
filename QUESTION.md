1.  Integer 内部维护着一个 IntegerCache 的缓存,默认缓存范围是 [-128, 127]，所以 [-128, 127] 之间的值用 == 和 != 比较也能能到正确的结果. 
所以Integer不是一个常量池，那是啥原理呢？
```
// operators/Equivalence.java
public class Equivalence {
    public static void main(String[] args) {
        Integer n1 = 47;
        Integer n2 = 47;
        System.out.println(n1 == n2);
        System.out.println(n1 != n2);
    }
}
true
false
```
