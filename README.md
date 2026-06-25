[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/KQahFieU)
Before running, install the middleware and associated tools (on both machines):
```
sudo dnf install python3-ice ice-compilers
```

This code is based on Example 3.21 of Maarten van Steen's book.

## Métodos da interface Printer (Printer.ice)

Além do `printString` original, a interface foi estendida com dois métodos novos:

| Método | Retorno | Descrição |
| --- | --- | --- |
| `printString(s)` | `string` | Imprime a string no servidor e retorna `s + "*"`. |
| `toUpper(s)` | `string` | Retorna a string convertida para maiúsculas. |
| `countChars(s)` | `int` | Retorna o número de caracteres da string. |

Após alterar o `Printer.ice`, regenere o stub com:
```
slice2py Printer.ice
```

Execute o servidor em uma máquina e o cliente na outra:
```
python3 server.py      # ou server2.py (dois objetos)
python3 client.py      # ou client2.py (dois proxies)
```
