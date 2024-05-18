
# Oque e Recursividade

A *recursividade* é uma técnica onde uma função chama a si mesma para resolver subproblemas menores e semelhantes ao problema original. É amplamente usada na ciência da computação para simplificar a solução de problemas complexos.

Abaixo Temos Alguns Exemplo

# 🌳Árvores:

*Travessia em Árvores*: Algoritmos como in-order, pre-order e post-order são naturalmente implementados de forma recursiva.

*Busca e Inserção em BST*: A busca e inserção em árvores binárias de busca (BST) são realizadas recursivamente, navegando pela árvore conforme os critérios de comparação.

## 🛠️Exemplos

```python
class Node:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None

def insert(node, value):
    if node is None:
        return Node(value)
    if value < node.value:
        node.left = insert(node.left, value)
    else:
        node.right = insert(node.right, value)
    return node

def search(node, value):
    if node is None or node.value == value:
        return node
    if value < node.value:
        return search(node.left, value)
    return search(node.right, value)

```
# 🗒️Listas:

*Ordenação*: Algoritmos de ordenação como QuickSort e MergeSort utilizam recursividade para dividir a lista em sublistas menores e ordená-las.
Exemplo de QuickSort:

```python

def quicksort(arr):
    if len(arr) <= 1:
        return arr
    pivot = arr[len(arr) // 2]
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    return quicksort(left) + middle + quicksort(right)
    
```








## 🌐Referência

 - [Oque e Recursividade ?](https://embarcados.com.br/recursividade/)
 - [Oque e Arvores na estrutura de dados ?](https://www.freecodecamp.org/portuguese/news/tudo-o-que-voce-precisa-saber-sobre-estruturas-de-dados-em-arvore/)


## 🙏Ajudas

- [@santhiagoepic](https://github.com/santhiagoepic)

