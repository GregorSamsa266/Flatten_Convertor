# Flatten_Convertor
a = [[1,'a',['cat'],2],[[[3]],'dog'],4,5]
def flatten_converter(a):
    flattened = []
    for item in a:
        if isinstance(item, list):
            flattened.extend(flatten_converter(item))
        else:
            flattened.append(item)
    return flattened

b = flatten_converter(a)
print(b)
#Reserved
list_1 = [[1, 2], [3, 4], [5, 6, 7]]

def reverse(list_1):
    reversed = []
    for item in list_1[::-1]:
        if isinstance(item, list):
            reversed.append(reverse(item))
        else:
            reversed.append(item)
    return reversed

list_2 = reverse(list_1)
print(list_2)
