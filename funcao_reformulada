def cabeca(lista):
    return lista[0]

def cauda(lista):
    return lista[1:]

def tamanho(lista):
    if lista == []:
        return 0
    else:
        return tamanho(cauda(lista)) + 1   

def soma(lista):
    if tamanho(lista) == 0:
        return 0
    else:
        return cabeca(lista) + soma(cauda(lista))

def menor2(x, y):
    if x < y:
        return x
    else:
        return y

def menor(l):
    if tamanho(l) == 1:
        return cabeca(l)
    else:
        menor_cauda = menor(cauda(l))
        return menor2(cabeca(l), menor_cauda)

def retElem(l, x):
    if x == cabeca(l):
        return cauda(l)
    else:
        resto = retElem(cauda(l), x)
        return [cabeca(l)] + resto

def selecao(l):
    if not l:
        return []
    else:
        menor_elem = menor(l)
        lista_sem_menor = retElem(l, menor_elem)
        return [menor_elem] + selecao(lista_sem_menor)

# Exemplos de uso:
if __name__ == "__main__":
    lista_teste = [5, 2, 8, 1, 9, 3]
    
    print(f"Lista original: {lista_teste}")
    print(f"Menor elemento: {menor(lista_teste)}")
    print(f"Lista sem o elemento 2: {retElem(lista_teste, 2)}")
    print(f"Lista ordenada: {selecao(lista_teste)}")
