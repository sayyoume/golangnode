## 函数

### 变长函数

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
```

