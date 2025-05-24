# plan-populations-graph-for-python

#four plant population graph for 12 year

import numpy as np
import matplotlib.pyplot as plt

# time values in x -axis
t = np.arange(0, 13, 1) #from o to 13 (0-1-...-12)
# y values
y1  = [0, 595, 220, 614, 452, 727, 702, 932, 1007, 1240, 1403, 1676, 1934]
y2 = [50,291, 164, 323, 280, 400, 413, 524, 583, 704, 807, 956, 1109]
y3 = [50, 17, 51, 36, 60, 57, 77, 83, 102, 115, 138, 159, 188]
y4 = [0,21, 9, 23, 18, 28, 27, 36, 39, 48, 55, 65, 75]

# plotting graph
plt.figure(figsize=(12, 6))
plt.plot(t, y1, color='hotpink', marker='o', linestyle='-', label="Age Group 1")
plt.plot(t, y2, color='orange',marker='*', linestyle='-',  label="Age Group 2")
plt.plot(t, y3, color='orangered',marker='^', linestyle='-',  label="Age Group 3")
plt.plot(t, y4, color='green',marker='s', linestyle='-',  label="Age Group 4")
plt.xlabel("Time t")
plt.ylabel("Population size $x_t$")
plt.title(r"$x_0 = (0,50,50,0)$")

plt.xticks(np.arange(0, 13, 2))  # X axis 0-2-4-6-8-10-12
plt.yticks(np.arange(0, 2200, 200))  # Y axis 0-200-400-...-2000
plt.grid(True)
plt.legend()
plt.show()
