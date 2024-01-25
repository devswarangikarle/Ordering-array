# Ordering-array
An array b1, b2 ,…, bn of positive integers is good if all the sums of two adjacent elements are equal to the same value. More formally, the array is good if there exists a k such that b[1] + b[2] = b[2] + b[3] = … = b[n−1] + b[n] = k . 

n = int(input())
a = list(map(int, input().split()))

# Sort the array
a.sort()

# Check if all adjacent elements have the same sum
sum_value = a[0] + a[-1]
for i in range(n - 1):
    if a[i] + a[i + 1] != sum_value:
        print("No")
        break
else:
    print("Yes")
