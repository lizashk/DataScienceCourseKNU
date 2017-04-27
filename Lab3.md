1. Функція add2(x, y), яка повертає суму двох чисел.

> add2<-function(x,y){
+ x+y
+ }
> add2(7, 9)
[1] 16

2. Функція above(x, n), яка приймає вектор та число n, та повертає всі елементі вектору, які більше n. По замовчуванню n = 10.

> above <-function(x,n=10){
+ x[x>n]
+ }
> v<-c(1,7,19,77,9,333,11)
> above(v,10)
[1]  19  77 333  11

3. Функція my_ifelse(x, exp, n), яка приймає вектор x, порівнює всі його елементи за допомогою exp з n, та повертає елементи вектору, які відповідають умові expression. Наприклад, my_ifelse(x, “>”, 0) повертає всі елементи x, які більші 0. Exp може дорівнювати “<”, “>”, “<=”, “>=”, “==”. Якщо exp не співпадає ні з одним з цих виразів, повертається вектор x.

> my_ifelse<-function(x,exp,n){
+ if (exp=="<") y<-x[x<n]
+ else if (exp==">") y<-x[x>n]
+ else if (exp=="<=") y<-x[x<=n]
+ else if (exp==">=") y<-x[x>=n]
+ else if (exp=="==") y<-x[x==n]
+ else y<-x
+ y
+ }
> my_ifelse(c(3,5,1,66,8,2,4), "<", 4)
[1] 3 1 2
> my_ifelse(c(3,5,1,66,8,2,4), ">", 4)
[1]  5 66  8
> my_ifelse(c(3,5,1,66,8,2,4), "<=", 4)
[1] 3 1 2 4
> my_ifelse(c(3,5,1,66,8,2,4), ">=", 4)
[1]  5 66  8  4
> my_ifelse(c(3,5,1,66,8,2,4), "==", 4)
[1] 4


4. Функція columnmean(x, removeNA), яка розраховує середнє значення (mean) по кожному стовпцю матриці, або data frame. Логічний параметр removeNA вказує, чи видаляти NA значення. По замовчуванню він дорівнює TRUE.

> columnmean<- function(x, removeNA=TRUE){
+ for (i in seq_len(ncol(x))) {
+ print(mean(x[,i],trim=0,na.rm=removeNA))
+ }
+ }
> mat_na = matrix( c(1, NA, 4, 8), 2, 2 )
> mat_na
     [,1] [,2]
[1,]    1    4
[2,]   NA    8
> columnmean(mat_na)
[1] 1
[1] 6
> columnmean(mat_na, FALSE)
[1] NA
[1] 6
> d_frame <- data.frame(abc = 1:4, vjuk = 3:6)
> columnmean(d_frame)
[1] 2.5
[1] 4.5
