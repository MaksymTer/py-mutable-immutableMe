# Given variables (Example)
a = 123
b = []
c = "Hi!"
d = [1, 2]
e = (3, 4)  # Immutable tuple
f = {"key": "value"}  # Mutable dictionary
g = {1, 2, 3}  # Mutable set
h = 3.14  # Immutable float

# Helper function to check if an object is mutable
def is_mutable(obj):
    try:
        obj.__hash__  # Immutable objects are hashable
        return False
    except TypeError:
        return True

# Sorting variables into "mutable" and "immutable"
sorted_variables = {
    "mutable": [var for var in [a, b, c, d, e, f, g, h] if is_mutable(var)],
    "immutable": [var for var in [a, b, c, d, e, f, g, h] if not is_mutable(var)]
}

# Output the result
print(sorted_variables)
