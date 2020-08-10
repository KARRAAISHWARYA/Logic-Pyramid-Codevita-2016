def element(i):
    first = 6
    second = 28
    if i == 1:
        return first
    if i==2:
        return 28
    for x in range(3, i+1):
        next = (second*2)-first+16
        first = second
        second = next
    return next
 
 
k = int(input())
for case in range(k):
    n = int(input())
    i=1
    for row in range(1,n+1):
        print((n-row)*"   ",end ='')
        for j in range(1, row+1):
            print(format(element(i),'05'), end = ' ')
            i+=1
        print()
