#loop 迴圈

以 c 來說迴圈有 for , while , do while 三個關鍵字. 在 go 裡面只有一個 for 來達到全部. 其實在 c 裡面也是可以只用 for 就夠了. 


以 for 迴圈來說 c 為

~~~
int i = 0;
for( i  = 0 ; i < 10 ; ++i )
{
    sum += i;
}
~~~

以下為 go 的 for 迴圈範例

~~~
sum := 0
for i := 0 ; i < 10 ; ++i {
    sum += i
}
~~~

從範例中可以看到 "( )" 省略了, 再來兩個中夸號並不是對齊的. 不對齊這件事情和我原本的習慣不同, 花了點時間去適應. 

 
c 的 do while 迴圈

~~~
int i = 0;

do{
    i += 1
}while( i < 10 );
~~~

go 中為

~~~
i := 0
for i < 100 {
    i += 1
}
~~~

c 的無限 while 迴圈

~~~
while(1)
{
   
}
~~~

go 的

~~~
for {

}
~~~

以上為 go 和 c 的迴圈使用比較. 從中可以了解一些語法上的差別