A = (5,10,21,32,56,77,90,115)

izq = 0 
der = len(A) - 1
cen = (izq + der) // 2 

n = int(input('Ingrese un número: '))
encontrar = False

while (izq <= der and encontrar == False):
    if A[cen] == n:
        encontrar = True
    elif n < A[cen]:
        der = cen - 1
    else:
        izq = cen + 1
    
    cen = (izq + der) // 2

if encontrar:
    print("Número encontrado en la posición:", cen)
else:
    print("Número no encontrado")
