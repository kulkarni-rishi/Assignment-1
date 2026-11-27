# ==========================================
# 1. LIST OPERATIONS (Mutable Sequence)
# ==========================================
print("=== LIST OPERATIONS ===")
fruits = ["apple", "banana", "cherry"]
print("Initial List:", fruits)

# Append & Insert
fruits.append("mango")
fruits.insert(1, "orange")
print("After append & insert:", fruits)

# Extend & Update
fruits.extend(["grapes", "banana"])
fruits[0] = "green apple"
print("After extend & update:", fruits)

# Count, Index & Sort
print("Count of 'banana':", fruits.count("banana"))
print("Index of 'cherry':", fruits.index("cherry"))
fruits.sort()
print("Sorted List:", fruits)

# Remove & Pop
fruits.remove("banana")      # removes first occurrence
popped_fruit = fruits.pop()  # removes and returns last item
print("Popped item:", popped_fruit)
print("List after remove & pop:", fruits)


# ==========================================
# 2. TUPLE OPERATIONS (Immutable Sequence)
# ==========================================
print("\n=== TUPLE OPERATIONS ===")
# Creating tuples (including single-element tuple with trailing comma)
colors = ("red", "green", "blue", "red")
single_item_tuple = ("yellow",)
print("Initial Tuple:", colors)
print("Single-element Tuple:", single_item_tuple, type(single_item_tuple))

# Indexing, Slicing & Length
print("First element:", colors[0])
print("Sliced tuple (1:3):", colors[1:3])
print("Length of tuple:", len(colors))

# Tuple Methods: count() and index()
print("Count of 'red':", colors.count("red"))
print("Index of 'blue':", colors.index("blue"))

# Concatenation & Repetition (creates new tuples)
combined_tuple = colors + single_item_tuple
repeated_tuple = single_item_tuple * 3
print("Concatenated Tuple:", combined_tuple)
print("Repeated Tuple:", repeated_tuple)

# Tuple unpacking (assignment)
c1, c2, c3, c4 = colors
print("Unpacked values:", c1, c2, c3, c4)

# "Appending" or "Removing" in a Tuple via list conversion
temp_list = list(colors)
temp_list.append("purple")
temp_list.remove("green")
colors_modified = tuple(temp_list)
print("Modified Tuple (via list):", colors_modified)


# ==========================================
# 3. DICTIONARY OPERATIONS (Key-Value Pairs)
# ==========================================
print("\n=== DICTIONARY OPERATIONS ===")
student = {
    "name": "Aarav",
    "roll_no": 101,
    "course": "B.Tech CSE",
    "marks": 88
}
print("Initial Dictionary:", student)

# Access values using key or get()
print("Name:", student["name"])
print("Grade (default if missing):", student.get("grade", "Not Assigned"))

# Add new key-value pair & Update existing value
student["branch"] = "AI & DS"
student.update({"marks": 92, "semester": 3})
print("After adding & updating:", student)

# Keys, Values & Items views
print("Keys:", list(student.keys()))
print("Values:", list(student.values()))
print("Items:", list(student.items()))

# Remove items using pop(), popitem(), and del
removed_marks = student.pop("marks")
last_key, last_val = student.popitem()  # removes last inserted item (Python 3.7+)
del student["roll_no"]
print("Removed marks:", removed_marks)
print("Popped last item:", (last_key, last_val))
print("Dictionary after removals:", student)

# Copy & Clear
student_copy = student.copy()
student.clear()
print("Cleared original dict:", student)
print("Copied dict preserved:", student_copy)
