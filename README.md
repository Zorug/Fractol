# 🌀 Fractol - Fractals in C with MiniLibX

This project was developed as part of the 42 School curriculum. It generates and allows interactive exploration of mathematical fractals using the lightweight graphics library [MiniLibX](https://harm-smits.github.io/42docs/libs/minilibx).

## 📸 Demo

![Burning Ship Fractal](https://github.com/Zorug/fractol/blob/main/fractols-gif/burning_ship.gif?raw=true)

*A live rendering of the Burning Ship fractal with dynamic zoom based on mouse position. The detail increases with each zoom level, revealing the self-similar structure of the fractal.*

---

## 🚀 Features

- Real-time rendering of fractals:
  - Mandelbrot
  - Julia (with custom parameters)
  - Burning Ship
- Zoom using mouse scroll
- Optional keyboard navigation
- CLI parameter selection
- Memory leak-free (verified with Valgrind ✅)

---

## 🧠 Mathematical Background

Fractals are generated through iterative formulas in the complex plane:

- **Mandelbrot:**  
  Zₙ₊₁ = Zₙ² + C, with Z₀ = 0

- **Julia:**  
  Zₙ₊₁ = Zₙ² + C, with Z₀ as the pixel position and C defined by the user

- **Burning Ship:**  
  Zₙ₊₁ = (|Re(Zₙ)| + i·|Im(Zₙ)|)² + C

---

## ⚙️ How to Compile

### This project is Linux-compatible and requires MiniLibX.

### 1. Install dependencies (Debian/Ubuntu):
sudo apt-get install libx11-dev libxext-dev libbsd-dev

### 2. Clone the repository:
git clone https://github.com/Zorug/fractol.git
cd fractol

### 3. Compile:
make

---

## 🖥️ How to Run

./fractol <fractal_type>

### Available fractal types:
- `julia` → Julia Set
- `mandelbrot` → Mandelbrot Set
- `burning_ship` → Burning Ship

### Example:
./fractol julia

If you choose `julia`, the program will ask you to input the real and imaginary parts of `C`.

---

## 🖱️ Controls

| Action            | Input            |
|-------------------|------------------|
| Zoom in/out       | Mouse scroll     |
| Close window      | `ESC` key or X button |
| Change iterations | Optional mouse/key inputs |

---

## 🔎 Validation

Verified with:
- `valgrind` → No memory leaks
- `norminette` → 42 style guide (if applicable)

---

## 👨‍💻 Author

| [<img src="https://avatars.githubusercontent.com/u/54179576?v=4" width=115><br><sub>Cassiano Gross</sub>](https://github.com/Zorug) | 
| :---: |

---

## 📄 License

This project is part of the 42 School educational curriculum. For educational and personal use only.

