# visionMashine
# q1
import matplotlib.pyplot as plt
import matplotlib.patches as patches

fig, ax = plt.subplots(figsize=(6, 6))

ax.set_xlim(0, 500)
ax.set_ylim(0, 500)
ax.set_aspect('equal')
ax.invert_yaxis()

rectangles = [
    ((100, 100), 50, 100),
    ((200, 200), 100, 100),
    ((250, 320), 150, 80)
]

for (x, y), w, h in rectangles:
    rect = patches.Rectangle((x, y), w, h, linewidth=2, edgecolor='r', facecolor='none')
    ax.add_patch(rect)

plt.title("Rectangles - Matplotlib")
plt.grid(True)
plt.show()

