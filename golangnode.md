## 函数

### 1.变长函数

 在参数列表最后类型名称之前增加省略号“...” 就可以声明称一个变长函数

```go
func sum(values ...int) int{
    sum :=0
    for _,val :=range values{
        sum += val
    }
    return sum
}

//测试代码
fmt.Println(sum()) 			//0
fmt.Println(sum(1)) 		//1
fmt.Println(sum(1,2,3,4))   //10

values :=[]int{1,2,3,4}
fmt.Println(sum(values...))
```

### 2.方法

方法的声明和函数类似，只是在函数名字前多了一个参数

```go
//普通函数
func abc(a,b int) int{
    return a+b
}
```

## 切片

### 1.声明切片

```go
var strList []string //字符串切片
var numList []int	//整型切片
var numListEmpty = []int{] //声明一个空切片
//使用make构造切片
make([]T,size,cap)
 /*
  * T 切片类型                        
  * size为这个类型分配多少个元素
  * cap 预分配元素数量，不影响size，可以提前分配空间
  */
 a :=make([]int,2)
 b := make([]int,2,10)

 fmt.Println(a,b)
 fmt.Println(len(a),len(b),cap(a),cap(b))       
 输出：
 [0 0] [0 0]
 2 2 2 10
```

## channel

```go
var c chan int // c==nil
c :=make(chan int)
c <- 1
c <- 2
n := <- c
fmt.Println(n)
```







































