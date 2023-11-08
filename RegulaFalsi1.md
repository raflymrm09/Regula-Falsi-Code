# SPNL-Regula-Falsi

Tugas Metode Nmerik di GitHub oleh Anggay Luri Pramana


# Regula-Falsi-Code

def f(x):
return x**2 - 6*x + 5

def find_root_bisection(a, b, tolerance):
if f(a) * f(b) >= 0:
    print("Tidak ada akar dalam selang ini.")
    return None

while (b - a) / 2 > tolerance:
    midpoint = (a + b) / 2
    if f(midpoint) == 0:
        return round(midpoint, 3)
    elif f(a) * f(midpoint) < 0:
        b = midpoint
    else:
        a = midpoint

return round((a + b) / 2, 3)

a = 3
b = 6
tolerance = 0.001

root = find_root_bisection(a, b, tolerance)
if root is not None:
    print(f"Akar persamaan f(x) = x^2 - 6x + 5 = 0 dalam selang [{a}, {b}] adalah {root}")

_hasil dari coding diatas adalah Akar Persamaan = 5.0_
