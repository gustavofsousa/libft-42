<h1 align="center">libft</h1>

<p align="center">
  <img src="https://img.shields.io/badge/linguagem-C-blue.svg" alt="Linguagem">
  <img src="https://img.shields.io/badge/42-School-black.svg" alt="42 School">
  <img src="https://img.shields.io/badge/status-completo-brightgreen.svg" alt="Status">
</p>

<p align="center">
  Uma reimplementação completa da biblioteca padrão C — do zero, sem usar nenhuma das funções originais.
</p>

<p align="center">
  <a href="README.md">🇺🇸 Read in English</a>
</p>

---

## Por que este projeto importa

> "Este projeto me ensinou como a biblioteca padrão do C funciona por baixo dos panos — como strings são percorridas byte a byte, como a memória é alocada e manipulada manualmente, e o que realmente significa escrever código confiável e reutilizável."

Entender esses fundamentos é o que separa um desenvolvedor que *usa* ferramentas de um que as *compreende*. Todo engenheiro sênior que trabalha com sistemas, embarcados ou ambientes críticos de performance pensa nesse nível de abstração.

---

## O que foi construído

Uma biblioteca C pessoal e funcional (`libft.a`) cobrindo:

### Memória
| Função | Descrição |
|---|---|
| `ft_memset` | Preenche área de memória com um byte |
| `ft_bzero` | Zera uma área de memória |
| `ft_memcpy` | Copia áreas de memória |
| `ft_memmove` | Cópia segura com tratamento de sobreposição |
| `ft_memchr` | Localiza byte na memória |
| `ft_memcmp` | Compara áreas de memória |
| `ft_calloc` | Aloca e inicializa memória com zero |

### Strings
| Função | Descrição |
|---|---|
| `ft_strlen` | Comprimento de string |
| `ft_strdup` | Duplica uma string |
| `ft_strchr` / `ft_strrchr` | Busca de caractere |
| `ft_strncmp` | Comparação de strings |
| `ft_strlcpy` / `ft_strlcat` | Cópia e concatenação seguras |
| `ft_strnstr` | Busca de substring |
| `ft_substr` | Extrai substring |
| `ft_strjoin` | Une duas strings |
| `ft_strtrim` | Remove caracteres das bordas |
| `ft_split` | Divide string por delimitador |
| `ft_strmapi` / `ft_striteri` | Map funcional sobre string |

### Conversão
| Função | Descrição |
|---|---|
| `ft_atoi` | String para inteiro |
| `ft_itoa` | Inteiro para string |
| `ft_toupper` / `ft_tolower` | Conversão de case |

### Saída
| Função | Descrição |
|---|---|
| `ft_putchar_fd` | Escreve char em file descriptor |
| `ft_putstr_fd` | Escreve string em file descriptor |
| `ft_putendl_fd` | Escreve string + newline |
| `ft_putnbr_fd` | Escreve inteiro |

### Listas Ligadas (Bônus)
| Função | Descrição |
|---|---|
| `ft_lstnew` | Cria novo nó |
| `ft_lstadd_front` / `ft_lstadd_back` | Adiciona nó ao início/fim |
| `ft_lstsize` | Conta nós da lista |
| `ft_lstlast` | Obtém último nó |
| `ft_lstdelone` / `ft_lstclear` | Remove nó(s) |

---

## Um detalhe técnico que se destaca

A implementação do `ft_split` trata corretamente casos como delimitadores consecutivos, delimitadores no início/fim da string e strings vazias — situações onde implementações ingênuas falham silenciosamente ou vazam memória. Isso demonstra atenção aos casos de borda, não apenas ao caminho feliz.

---

## Como usar

```bash
git clone https://github.com/gustavofsousa/libft-42.git
cd libft-42
make
```

Isso gera `libft.a`. Para usar no seu projeto:

```c
#include "libft.h"
```

Compile com:
```bash
gcc seu_arquivo.c -L. -lft -o seu_programa
```

### Targets do Makefile

| Target | Ação |
|---|---|
| `make` | Compila a biblioteca |
| `make bonus` | Compila com funções de lista ligada |
| `make clean` | Remove arquivos objeto |
| `make fclean` | Remove objetos e biblioteca |
| `make re` | Recompila tudo |

---

## Habilidades demonstradas

- Gerenciamento manual de memória em C
- Aritmética de ponteiros e manipulação de strings
- Makefile e criação de biblioteca estática (`ar`)
- Programação defensiva e tratamento de casos extremos
- Implementação de estrutura de dados lista ligada

---

## Licença

Este projeto foi desenvolvido como parte do currículo da [42 School](https://42.fr).

---

<p align="center">Feito com ☕ na 42 Rio de Janeiro</p>
