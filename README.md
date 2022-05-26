# Matrix-randomizer

```
[X]: # Language: c
[X]: # Path: randomizer.c
```

### Objetivo
Criar um algoritmo que gere uma lista de números aleatórios com o objetivo de randomizar uma matriz de 3 nível com 
2 linhas, 4 colunas e 8 char dentro dessa última lista.
<br>
Com este algoritmo clonar uma matriz de base em uma matriz randomizada através dos índices gerados.
<br>

### Check-list
```
[X] Gerar uma lista aleatória com tamanho dinamico.
[X] Quebrar a lista gerada em 2 linhas tendo metade em cada.
[X] Espelhar a lista base na lista randomizada utilizando os indices gerados.
```

### Funcionamento

#### Randomização.
Utilizando uma lista vazia, e um índice aleatório, o valor retornado da busca na lista é o endereço de mória referente
ao armanezamento do valor na lista.
Sendo assim, o valor é divido pelotamanho da lista requisitada e o resto da operação é adionado a lista caso o valor 
ainda não esteja presente na mesma.

<br>

````C
base[2][4][8] = {
            {
                'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h',
                'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p',
                'q', 'r', 's', 't', 'u', 'v', 'w', 'x',
                'y', 'z', 'a', 'b', 'c', 'd', 'e', 'f'
            },
            {
                '1', '2', '3', '4', '5', '6', '7', '8',
                '9', '0', '1', '2', '3', '4', '5', '6',
                '7', '8', '9', '0', '1', '2', '3', '4',
                '5', '6', '7', '8', '9', '0', '1', '2'
            }
    }
````
<br>

##### Exemplo de lista gerada.

````C
//lista de 8 itens
int itens[8] = [0, 3, 5, 2, 1, 4, 6, 7]
````
Após a criação da lista de 8 itens é necessário quebra-la em 2 linhas tendo metade em cada.
Alternando os itens entre cada linha, ou seja, a primeira linha terá os itens 0, 3, 5, 2 e a segunda terá os itens 
1, 4, 6, 7.
<br>

##### Exemplo de lista quebrada.
````C
//lista de 2 linhas e 4 colunas
int arr[2][4]= [ [ 0, 5, 1, 6 ], [ 3, 2, 4, 7 ] ]
````

#### Clonagem.
A partir do momento que a lista aleatória é gerada, é necessário que seja feita a clonagem da lista base para a lista
randomizada, ou seja, a lista randomizada terá os mesmos valores da lista base porém com os índices da lista quebrada
que geramos anteriormente.
<br>
Resultando então na lista final randomizada.
````C
//lista de 2 linhas e 4 colunas e 8 char randomizada.
{
    {
        {'7' '8' '9' '0' '1' '2' '3' '4'}
        {'i' 'j' 'k' 'l' 'm' 'n' 'o' 'p'}
        {'q' 'r' 's' 't' 'u' 'v' 'w' 'x'}
        {'y' 'z' 'a' 'b' 'c' 'd' 'e' 'f'}
    },
    {
        {'a' 'b' 'c' 'd' 'e' 'f' 'g' 'h'}
        {'1' '2' '3' '4' '5' '6' '7' '8'}
        {'9' '0' '1' '2' '3' '4' '5' '6'}
        {'5' '6' '7' '8' '9' '0' '1' '2'}
    }
};
````

# FIM :D
