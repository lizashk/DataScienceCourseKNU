1. Створити змінні базових (atomic) типів. Базові типи: character, numeric, integer, complex, logical.
> char<-"liza"
> char
[1] "liza"
> numer<-0.7
> numer
[1] 0.7
> integ<-7L
> integ
[1] 7
> compl<-3i+7
> compl
[1] 7+3i
> logic<-FALSE
> logic
[1] FALSE
2. Створити вектори, які: містить послідовність з 5 до 75; містить числа 3.14, 2.71, 0, 13; 100 значень TRUE.
> x<-c(5:75)
> x
 [1]  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21
[18] 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38
[35] 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55
[52] 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72
[69] 73 74 75
> y<-c(3.14, 2.71, 0, 13)
> y
[1]  3.14  2.71  0.00 13.00
> z<-replicate(100, c(TRUE))
> z
  [1] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
 [11] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
 [21] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
 [31] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
 [41] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
 [51] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
 [61] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
 [71] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
 [81] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
 [91] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
3. Створити наступну матрицю за допомогою matrix, та за допомогою cbind або rbind
0.5 1.3 3.5
3.9 131 2.8
0 2.2 4.6
2 7 5.1

> matrix(c(0.5, 3.9, 0, 2, 1.3, 131, 2.2, 7, 3.5, 2.8, 4.6, 5.1), ncol=3, nrow=4)
     [,1]  [,2] [,3]
[1,]  0.5   1.3  3.5
[2,]  3.9 131.0  2.8
[3,]  0.0   2.2  4.6
[4,]  2.0   7.0  5.1
> col1<-c(0.5, 3.9, 0, 2)
> col2<-c(1.3, 131, 2.2, 7)
> col3<-c(3.5, 2.8, 4.6, 5.1)
> combi_matrix<-cbind(col1, col2, col3)
> combi_matrix
     col1  col2 col3
[1,]  0.5   1.3  3.5
[2,]  3.9 131.0  2.8
[3,]  0.0   2.2  4.6
[4,]  2.0   7.0  5.1
4. Створити довільний список (list), в який включити всі базові типи.
> list("liza", 0.7, 7L, 3i+7, FALSE)
[[1]]
[1] "liza"

[[2]]
[1] 0.7

[[3]]
[1] 7

[[4]]
[1] 7+3i

[[5]]
[1] FALSE
5. Створити фактор з трьома рівнями «baby», «child», «adult».
> x<-c("baby", "child", "child", "adult", "adult", "adult")
> factor(x, levels=c("baby", "child", "adult"))
[1] baby  child child adult adult adult
Levels: baby child adult
6. Знайти індекс першого значення NA в векторі 1, 2, 3, 4, NA, 6, 7, NA, 9, NA, 11. Знайти кількість значень NA.
> match(NA, c(1, 2, 3, 4, NA, 6, 7, NA, 9, NA, 11))
[1] 5
> sum(is.na(c(1, 2, 3, 4, NA, 6, 7, NA, 9, NA, 11)))
[1] 3
7. Створити довільний data frame та вивести в консоль.
> d_f<-data.frame(first = c("say", "hi", "to", "people"), num = 1:4)
> d_f
   first num
1    say   1
2     hi   2
3     to   3
4 people   4
8. Змінити імена стовпців цього data frame.
> colnames(d_f)<-c("manners", "numbers")
> d_f
  manners numbers
1     say       1
2      hi       2
3      to       3
4  people       4
