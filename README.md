def burbuja(lista):
    n = len(lista)
    for i in range(n):
        intercambiado = False
        for j in range(0, n-i-1):
            if lista[j] > lista[j+1]:
                lista[j], lista[j+1] = lista[j+1], lista[j]
                intercambiado = True
        if not intercambiado:
            break
    return lista
numeros = [int(x) for x in input("Introduce una lista de números separados por espacios: ").split()]
print("Lista ordenada:", burbuja(numeros))
