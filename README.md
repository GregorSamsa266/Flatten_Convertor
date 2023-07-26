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
