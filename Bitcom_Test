# 1. MEAN COLOR 
from collections import Counter
import random

colors_by_day = {
    "MONDAY": ["GREEN", "YELLOW", "GREEN", "BROWN", "BLUE", "PINK", "BLUE", "YELLOW", "ORANGE", "CREAM", "ORANGE", "RED", "WHITE", "BLUE", "WHITE", "BLUE", "BLUE", "BLUE", "GREEN"],
    "TUESDAY": ["ARSH", "BROWN", "GREEN", "BROWN", "BLUE", "BLUE", "BLEW", "PINK", "PINK", "ORANGE", "ORANGE", "RED", "WHITE", "BLUE", "WHITE", "WHITE", "BLUE", "BLUE", "BLUE"],
    "WEDNESDAY": ["GREEN", "YELLOW", "GREEN", "BROWN", "BLUE", "PINK", "RED", "YELLOW", "ORANGE", "RED", "ORANGE", "RED", "BLUE", "BLUE", "WHITE", "BLUE", "BLUE", "WHITE", "WHITE"],
    "THURSDAY": ["BLUE", "BLUE", "GREEN", "WHITE", "BLUE", "BROWN", "PINK", "YELLOW", "ORANGE", "CREAM", "ORANGE", "RED", "WHITE", "BLUE", "WHITE", "BLUE", "BLUE", "BLUE", "GREEN"],
    "FRIDAY": ["GREEN", "WHITE", "GREEN", "BROWN", "BLUE", "BLUE", "BLACK", "WHITE", "ORANGE", "RED", "RED", "RED", "WHITE", "BLUE", "WHITE", "BLUE", "BLUE", "BLUE", "WHITE"],
}

# Flatten all colors into one list
all_colors = [color for colors in colors_by_day.values() for color in colors]

# Frequency count
color_counts = Counter(all_colors)

# Mean color — most frequent (mode)
mean_color = color_counts.most_common(1)[0][0]
print(f"1. Mean color (mode) is: {mean_color}")

# 2. MOSTLY WORN COLOR
print(f"2. Mostly worn color is: {mean_color}")

# 3. MEDIAN COLOR (middle value when sorted alphabetically)
sorted_colors = sorted(all_colors)
median_color = sorted_colors[len(sorted_colors) // 2]
print(f"3. Median color is: {median_color}")

# 4. BONUS - VARIANCE OF COLORS (based on frequencies)
import statistics

frequencies = list(color_counts.values())
variance = statistics.variance(frequencies)
print(f"4. Variance of the color frequencies is: {variance:.2f}")

# 5. BONUS - PROBABILITY OF RED
red_count = color_counts.get("RED", 0)
prob_red = red_count / len(all_colors)
print(f"5. Probability of picking RED is: {prob_red:.2f}")

# 6. SAVE TO POSTGRESQL DATABASE (SQL commands)
print("6. SQL Commands to save color frequencies:")
for color, freq in color_counts.items():
    print(f"INSERT INTO color_frequencies (color, frequency) VALUES ('{color}', {freq});")

# 7. BONUS - RECURSIVE SEARCH
def recursive_search(lst, target, index=0):
    if index >= len(lst):
        return -1
    if lst[index] == target:
        return index
    return recursive_search(lst, target, index + 1)

numbers_list = [3, 6, 8, 12, 7, 10, 4, 9]
user_number = 7
found_index = recursive_search(numbers_list, user_number)
print(f"7. Recursive Search: Number {user_number} found at index {found_index}")

# 8. RANDOM 4-DIGIT BINARY TO BASE-10
binary_number = "".join(str(random.randint(0, 1)) for _ in range(4))
decimal_number = int(binary_number, 2)
print(f"8. Random 4-bit binary: {binary_number} => Base-10: {decimal_number}")

# 9. SUM OF FIRST 50 FIBONACCI NUMBERS
def fibonacci_sum(n):
    fib_seq = [0, 1]
    for _ in range(2, n):
        fib_seq.append(fib_seq[-1] + fib_seq[-2])
    return sum(fib_seq)

fib_sum = fibonacci_sum(50)
print(f"9. Sum of first 50 Fibonacci numbers is: {fib_sum}")
