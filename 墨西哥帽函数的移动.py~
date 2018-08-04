#-*-coding: utf-8-*-
import numpy as np
import matplotlib.pyplot as plt
import matplotlib.animation as animation

x = np.linspace(-20, 20, 5000)
psi = lambda x: (1 - x**2) * np.exp(-x**2 / 2)
y = psi(x)

fig, ax = plt.subplots()
line, = ax.plot(x, y)
a_0, b_0 = 2, 1
m, n = 1, -1

def update(i):
    global m, n
    y = psi(x / a_0**m - n * b_0)
    m, n = m - 0.01, n - 0.1
    line.set_data(x, y)
    return line

ani = animation.FuncAnimation(fig, update, np.arange(0, 2, 0.01), interval = 500)

plt.grid(True)
plt.show()
