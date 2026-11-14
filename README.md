# Mini Portal Interativo

Mini portal web com várias ferramentas do dia a dia reunidas em uma única página: login e cadastro simulados, calculadora, contador e cronômetro, lista de tarefas, conversores, gerador de senhas e galeria de imagens. Feito em 2025, em HTML, CSS e JavaScript puros, como projeto acadêmico do curso de Gestão da Tecnologia e Informação da Fatec Barueri.

O projeto **não usa banco de dados nem back-end**. Tudo roda no navegador, e os dados ficam salvos localmente com `localStorage`.

(ADICIONAR: print da tela inicial em uma pasta `docs/` e o link da versão online, se publicar no GitHub Pages: Settings > Pages > Branch `main`.)

## Funcionalidades

| Seção | O que faz |
| ----- | --------- |
| **Início** | Painel com atalhos para todas as ferramentas e campo de pesquisa para encontrar uma seção |
| **Login / Cadastro** | Cadastro de usuário (nome, e-mail e senha) com aviso de usuário já existente, e login com verificação. O nome do usuário aparece no topo e continua após recarregar a página |
| **Calculadora** | Soma, subtração, multiplicação e divisão com teclado na tela, botão de limpar e aviso de expressão inválida |
| **Contador / Cronômetro** | Contador com aumentar, diminuir e reset, que guarda o valor no navegador. Cronômetro (hh:mm:ss) com start, stop e reset |
| **Lista de tarefas** | Adicionar, marcar como concluída e remover tarefas, salvas no navegador. O texto é escapado antes de ser exibido, para não interpretar HTML digitado |
| **Conversor** | Temperatura (°C e °F) e moeda (BRL e USD) com cotação fixa de 5,20, apenas como estimativa |
| **Gerador de senhas** | Tamanho de 4 a 64 caracteres (padrão 16), com opções de maiúsculas, números e símbolos, e botão para copiar |
| **Galeria** | 6 imagens com visualização ampliada (lightbox): clique para ampliar e clique de novo para fechar |

Além disso, o portal tem:

- Tema claro e escuro, com a escolha salva no navegador
- Relógio com data na barra lateral
- Layout responsivo, com a barra lateral passando para o topo em telas pequenas

## Tecnologias

- HTML5
- CSS3 (variáveis CSS, Grid e Flexbox)
- JavaScript puro, sem frameworks
- Web Storage (`localStorage`)
- Fonte Inter, do Google Fonts

As imagens da galeria vêm do [Lorem Picsum](https://picsum.photos), então a galeria e a fonte precisam de conexão com a internet. O restante funciona offline.

## Como executar

Não precisa instalar nada.

1. Baixe o repositório ou clone:

```bash
git clone https://github.com/HebertFD/MiniPortalinterativo.git
```

2. Abra o arquivo `MiniPortalinterativo.html` no navegador (clique duas vezes nele).

## Dados salvos no navegador

Os dados ficam apenas no navegador de quem está usando, nas seguintes chaves do `localStorage`:

| Chave | Conteúdo |
| ----- | -------- |
| `mp_users` | Usuários cadastrados |
| `mp_user` | Usuário logado |
| `mp_todos` | Lista de tarefas |
| `mp_count` | Valor do contador |
| `mp_theme` | Tema escolhido (claro ou escuro) |

Limpar os dados do navegador apaga tudo isso.

## Limitações e pontos de atenção

Este é um projeto de estudo, e algumas partes são simplificadas de propósito:

- **O login é uma simulação.** As senhas ficam em texto puro no `localStorage`, então não use senhas reais. Em um sistema de verdade, o login precisa de um back-end, senhas com hash (como bcrypt ou Argon2) e sessões ou tokens.
- **O gerador de senhas usa `Math.random()`**, que não é seguro para fins criptográficos. Em uso real, o correto é `crypto.getRandomValues()`.
- **A calculadora avalia a expressão com `Function()`.** Funciona bem em um projeto local, mas é uma prática arriscada. Uma melhoria seria escrever um interpretador próprio de expressões matemáticas.
- **A cotação do conversor é fixa**, e não consulta valores reais.

## Próximos passos (ideias)

- Criar um back-end com banco de dados para o login e a lista de tarefas
- Consumir uma API de cotação de moedas
- Separar o HTML, o CSS e o JavaScript em arquivos diferentes
- Corrigir os pontos de segurança listados acima
- Adicionar mais ferramentas ao portal



## Autor

**Hebert Rocha Lima da Silva**
[GitHub](https://github.com/HebertFD) | [LinkedIn](https://www.linkedin.com/in/hebert-rocha999)
