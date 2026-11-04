# TaskBoard

Quadro de tarefas em uma única página (HTML, CSS e JavaScript puros, sem dependências).

- Três colunas: A fazer, Em andamento e Concluído
- Cards com título, descrição, prioridade (Alta, Média, Baixa) e prazo
- Criar, editar, arrastar (mouse e toque) e excluir cards, com desfazer
- Busca e filtro por prioridade
- Tarefas salvas no arquivo `data/tasks.json` deste repositório (nada fica no navegador)

## Como as tarefas são salvas

A página lê `data/tasks.json` pela API do GitHub e, a cada alteração, grava o arquivo de volta com um commit ("Atualiza tarefas do TaskBoard"). Mudanças feitas em sequência são agrupadas em um único commit.

Para gravar, a página precisa de um token de acesso pessoal:

1. Crie um token *fine-grained* em https://github.com/settings/personal-access-tokens/new
2. Em *Repository access*, escolha **Only select repositories** e marque `taskboard`
3. Em *Permissions → Repository permissions*, dê **Contents: Read and write**
4. Na página, clique em **Conectar ao GitHub** e cole o token

O token fica só na memória da aba. Se marcar "Lembrar o token neste navegador", apenas o token é guardado no navegador. Sem token, o quadro abre em modo somente leitura.

Como o repositório é público, o conteúdo de `data/tasks.json` também é público.

## Publicação

O site é publicado pelo GitHub Pages a partir da branch `main`.
