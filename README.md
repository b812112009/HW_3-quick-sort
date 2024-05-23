def quicksort(array):
    if len(array) <= 1:
        return array
    else:
        pivot = array[0]
        lesser = [x for x in array[1:] if x <= pivot]
        greater = [x for x in array[1:] if x > pivot]
        print(lesser,"[",pivot,"]",greater)
        return quicksort(lesser) + [pivot] + quicksort(greater)

array = [33, 67, 8, 13, 54, 119, 3, 84, 25, 41]
sorted_array = quicksort(array)
print("Sorted array:", sorted_array)


output:

[8, 13, 3, 25] [ 33 ] [67, 54, 119, 84, 41]
[3] [ 8 ] [13, 25]
[] [ 13 ] [25]
[54, 41] [ 67 ] [119, 84]
[41] [ 54 ] []
[84] [ 119 ] []
Sorted array: [3, 8, 13, 25, 33, 41, 54, 67, 84, 119]
