# Pershkrimi i punes
Ky projekt eshte realizuar ne kuader te lendes "Modelime ne Fizike" dhe perfshin perdorimin e Python per krijimin e grafikëve dhe analizave numerike.

## Detyra 1: Figura e stilizuar
Ne kete detyre u krijua nje grafik shkencor duke perdorur librarite NumPy dhe Matplotlib.
Funksioni i perdorur ishte:
f(t) = sin(t) + cos(2t)
Grafiku u stilizua me ngjyra, etiketa dhe u ruajt si figure.

import numpy as np
import matplotlib.pyplot as plt

# 1. Vektori i kohës
t = np.linspace(0, 10, 1000)

# 2. Funksioni
x = np.sin(t) + np.cos(2*t)

# 3. Stilizimi i grafikut
plt.figure(figsize=(10, 6))

plt.plot(t, x, color='pink', linewidth=2, linestyle='-',
         marker='o', markevery=50, label='f(t) = sin(t) + cos(2t)')

# Etiketat
plt.xlabel("Koha t", fontsize=12)
plt.ylabel("Vlera x(t)", fontsize=12)

# Titulli
plt.title("Group Signature Plot", fontsize=16)

# Grid
plt.grid(True, linestyle='--', alpha=0.6)

# Legjenda
plt.legend()

# Ruajtja e figurës
plt.savefig("signature_plot.png", dpi=300)

# Shfaqja
plt.show()

## Detyra 2: Krijimi i repository ne GitHub
U krijua nje repository me strukture te organizuar:
- src/ per kodin
- figures/ per grafiket
- README.md per pershkrimin e projektit
- requirements.txt per librarite

group-project/
│
├── src/
│   └── main.py
│
├── figures/
│   └── signature_plot.png
│
├── README.md
└── requirements.txt

## Detyra 3: Ushtrime me NumPy
Ne kete detyre u realizuan:
- Llogaritja e funksionit f(t) = sin(t) + 0.5cos(3t)
- Derivati numerik
- Integrali kumulativ
- Norma e vektorit
- Vlera maksimale, minimale dhe mesatarja

  import numpy as np

# 1. Vektori i kohës
t = np.linspace(0, 10, 1000)

# 2. Funksioni
f = np.sin(t) + 0.5 * np.cos(3*t)

# 3. Derivati numerik
df = np.gradient(f, t)

# 4. Integrali kumulativ
dt = t[1] - t[0]
integral = np.cumsum(f) * dt

# 5. Norma e vektorit
norm = np.linalg.norm(f)

# 6. Statistika
max_val = np.max(f)
min_val = np.min(f)
mean_val = np.mean(f)

# Print rezultatet
print("Maksimumi:", max_val)
print("Minimumi:", min_val)
print("Mesatarja:", mean_val)
print("Norma:", norm)

## Kontributet
- Jonida Klari: implementimi i kodit dhe analiza numerike
- Alda Xhika: krijimi dhe stilizimi i grafikut
- Arlinda Shkina: organizimi i projektit ne GitHub dhe dokumentimi 
- Alda Xhika: krijimi dhe stilizimi i grafikut
- Arlinda Shkina: organizimi i projektit ne GitHub dhe dokumentimi
