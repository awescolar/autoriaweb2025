# Autoria Web 2025 - Os pioneiros

## Como a Turma Vai Trabalhar com Fork no GitHub

Este é um guia simples para a turma colaborar no projeto usando GitHub.

---

### Passo 1: Fazer Fork do Projeto Original (feito pelo professor)
- **Fork** é fazer uma cópia do projeto de outra pessoa para a sua conta no GitHub.
- Assim você pode mexer nessa cópia sem atrapalhar o projeto original.
  

### Passo 2: Clonar o Fork no Computador
- **Clonar** significa copiar o projeto do GitHub para o seu computador, a partir da sua cópia, para trabalhar nele.
- No terminal (programa para digitar comandos), digite: `git clone https://github.com/{seu-user}/autoriaweb2025.git`
  _Isso cria uma pasta no computador com o projeto para você mexer._

### Passo 3: Configurar o Repositório Original como Upstream
- **Upstream** é o nome que damos para o projeto original do professor.
- Assim você pode puxar as novidades do projeto original, para manter seu fork atualizado.
- No terminal, dentro da pasta do projeto, digite: `git remote add upstream https://github.com/awescolar/autoriaweb2025`

### Passo 4: Sincronizar seu Fork com o Projeto Original
- **Sincronizar** é atualizar seu fork com as mudanças que o professor fez.
- Primeiro, vá para a branch principal (linha principal do projeto): `git checkout main`
- Depois, traga as novidades do projeto original: `git pull upstream main`


### Passo 5: Criar uma Branch para Cada Atividade
- **Branch** é uma linha separada para trabalhar em uma tarefa sem mexer no restante do projeto.
- Para cada tarefa, crie uma branch nova, assim: `git checkout -b nome-da-sua-branch`


### Passo 6: Fazer Commit e Enviar para o GitHub
- **Commit** é salvar suas mudanças no computador, com uma mensagem que explica o que você fez.
- Para enviar suas mudanças para o seu fork no GitHub, use os comandos:

`git add .`
`git commit -m "Descrição do que foi feito"`
`git push origin nome-da-sua-branch`


### Passo 7: Abrir um Pull Request
- No GitHub, vá para seu fork e abra um **Pull Request** na sua branch.
- Pull Request é um pedido para o professor revisar e aceitar suas mudanças no projeto original.
- O professor analisa e, se aprovar, junta seu código com o projeto principal.

---
## Resumo dos Comandos Mais Usados
- `git clone https://github.com/{seu-usuario}/autoriaweb2025.git`
- `git remote add upstream https://github.com/awescolar/autoriaweb2025`
- `git checkout main`
- `git pull upstream main`
- `git checkout -b nome-da-sua-atividade`
- `git add .`
- `git commit -m "Mensagem explicando a mudança"`
- `git push origin nome-da-sua-atividade`

Esse processo ajuda a turma a colaborar, mantendo tudo organizado e atualizado com as tarefas do professor.

---

### Práticas

**Atividade 3 | ```14 / 07```**

Nesta atividade iremos trabalhar na montagem de uma página completa: Montando a Página de Tipografia.

Os principais pontos dessa atividade são:

1. Separação em blocos usando a tag ```<section>```;
2. Alinhamento de blocos no centro, como um container;
3. Uso de Flebox para alinhar os itens.

### Instruções

1. **Acesse e veja** o código HTML da atividade que está na pasta ```/atv-3```.

2. **Crie seu arquivo local**: Depois, crie um arquivo chamado `seunome-tipografia.html`, no seu computador. Lembre-se de criar uma pasta com o mesmo nome da atividade, pois você precisará enviar para o GSA.

3. **Crie** o CSS skeleton em `style.css`, como o que tá na pasta da atividade-3 no Github.

4. **Integre o arquivo CSS e HTML**, localizados na mesma pasta. Depois, com seu arquivo CSS criado, desenvolva seu código CSS e também HTML.

5. **Utilize as cores** e as demais variáveis, para formatar seu projeto:

   - Solicite o arquivo Figma do projeto ao professor, para ver todos os detalhes.

6. **Entregue** ambos os arquivos no Google Sala de Aula (GSA).
   - Para esta entrega, você deverá enviar a pasta inteira do projeto em um arquivo **.zip**
   - Selecione a pasta, com o botão direito do mouse, selecione enviar para, arquivo zip (pasta compactada) e crie um arquivo com **seunome-atv-7.zip**
   - Envie o arquivo no GSA
  
---

**Atividade 2**

Nesta atividade você irá trabalhar com características muito parecidas com a atividade anterior. Alguns elementos deverão mudar, como:

1. A foto será diferente (alinhamento central, item arredondado).
2. Há ícones de estrelas para serem adicionados como imagens, um ao lado do outro.
3. O tamanho do botão é diferente e está alinhado ao centro.

Imagem de referência.
![image](https://github.com/user-attachments/assets/983373eb-62e3-414e-a059-a97bf2f6e9bb)

### Instruções

1. **Acesse e veja** o código HTML da atividade que está na pasta ´´´/atv-2´´´. Depois, crie um arquivo chamado `seunome-card.html`, no seu computador. Lembre-se de criar uma pasta com o mesmo nome, pois você precisará enviar para o GSA.

2. **Crie** o CSS skeleton em `seunome-card.css`.

3. **Integre o arquivo CSS e HTML**, localizado na mesma pasta. Depois, no seu arquivo CSS criado, desenvolva seu código.

4. **Utilize as cores** e as demais variáveis, para formatar seu projeto:

   - Cores usadas: #3B3F5C (nome, titulos e textos), #FFFFFF (cor do texto do botão) e #5D5FEF (background do botão).
   - Medidas em 24px de `padding` entre as bordas, 32px `padding` do topo, e 16px de `margin` entre os elementos internos;
   - Fontes (pode usar `font-family: Open Sans;`). Deve carregar do Google Fonts.

5. **Entregue** ambos os arquivos no Google Sala de Aula (GSA).
   - Selecione a pasta do projeto e crie um arquivo **seunome-atv-6.zip**
   - Envie o arquivo no GSA

**Atividade 1**

### Instruções

1. **Acesse e Copie** o código HTML da atividade que está na pasta ´´´/atv-1´´´. Depois, crie um arquivo chamado `seunome-card.html`, no seu computador.

2. **Crie** o CSS skeleton em `seunome-card.css`. A partir de agora você deverá criar um arquivo de CSS separado. Para deixar mais organizado.

3. **Acesse e copie o código** no arquivo CSS de exemplo, localizado na mesma pasta. Depois, no seu arquivo CSS criado, cole o código copiado.

4. **Preencha** cada comentário de CSS com valores reais:

   - Cores em hexadecimal ou RGB
   - Medidas em `px`, `%` ou `rem`
   - Fontes (pode usar `font-family: sans-serif;`)
   - Sombra com `box-shadow: 0 2px 6px rgba(0,0,0,0.1);`

5. **Abra** o HTML no navegador e ajuste até que o card fique visualmente igual ao exemplo:

   - Imagem em cima, corpo branco, cantos arredondados
   - Título grande, subtítulo menor
   - Parágrafo legível e botão destacado

6. **Entregue** ambos os arquivos no Google Sala de Aula (GSA).
   - Selecione a pasta do projeto e crie um arquivo **seunome-atv-5.zip**
   - Envie o arquivo no GSA
