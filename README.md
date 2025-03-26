Java Learn
====================

# 1 → Carregamento de memoria, array e listas
---------------------

> Variaveis cujo o tipo são classes não devem ser entendidas como caixas mas sim como ponteiros para a memoria.

![memory_ref](img/MEMORY-REFERENCE.png)

> Variaveis baseadas em em classes referenciam a um endereço de memoria.

###  1.1 → Tipos primitivos são tipos valor.
> Tipos primitivos de valor em Java, tipos primitivos são tipos valor, tipos valor são caixas e nao ponteiros para a memoria.

![memory_ref2](img/MEMORY-REFERENCE2.png)

> Se ``` y = x ``` então se cria uma copia do valor da variavel ``` y = 10``` .

### 1.2 → Tipos primitivos do Java

| Type     |    contains        | default   | size
| -------- |    --------        | -------   | ----
| boolean  | true or false      |  false    |  1 bit
| char     | unicode character  |  \u0000   |  16 bit
| byte     | signed integer     |  0        |  8 bits
| short    | signed integer     |  0        |  16 bits
| int      | signed integer     |  0        |  32 bits
| long     | signed integer     |  0        |  64 bits
| float    | floating point     |  0.0      |  32 bits
| double   | floating point     |  0.0      |  64 bits


### 1.3 → Valores padrão

> Quando alocamos New() ou qualquer dado estruturado (classe ou array) se assume valores padrão para seus elementos.

```Java
Product p = new Product();
```

![memory_ref3](img/MEMORY-REFERENCE3.png)

### 1.3 Tipos referência vs. tipos valor

| classe | tipo primitivo
| ---  | ---
| Vantagem: usufrui de todos recursos OO | Vantagem: é mais simples e mais performatico
| Variáveis são ponteiros | Variáveis são caixas
| Objetos precisam ser instanciadas usando new, ou apontar para um objeto já existente. | Não instancia. Uma vez declarados, estão prontos para uso.
| Aceita valor null | Não aceita valor null
| ``` y = x ``` Y passa a apontar para onde X aponta | ``` y = x ``` Y recebe uma cópia de X
| Objetos instanciados no heap | objetos instanciados no stack 
| Objetos não utilizados são desalocados em um momento próximo pelo garbage collector | Objetos são desalocados imediatamente quando seu escopo de execução é finalizado.

> EX:
> ![memory_ref4](img/MEMORY-REFERENCE4.png)
> neste exemplo mesmo ```p``` sendo uma variável de escopo ela utiliza de uma referencia em memoria para lidar com os dados. 

# 2 → Vetores
---------------------