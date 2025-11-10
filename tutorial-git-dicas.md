# Manual GitHub – Receita para as Tarefas (Windows + VSCode)

Este manual é um guia passo a passo para você trabalhar com as tarefas no GitHub.  
Siga as etapas como uma receita de bolo.  

---

## 1. Configurar usuário no computador
Diga quem você é para o Git:
```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@ifrn.edu.br"
```
👉 Se aparecer nome/email de outra pessoa → troque com os comandos acima.  

---

## 2. Criar o fork do repositório do professor
1. No GitHub, abra o repositório oficial.  
2. Clique em **Fork** (canto superior direito).  
3. Escolha a sua conta pessoal.  

👉 Agora você tem sua própria cópia do repositório.  

---

## 3. Clonar seu fork
Baixe para seu computador:
```bash
git clone https://github.com/seu-usuario/seu-fork.git
cd seu-fork
```

Você deve fazer isso sempre que precisar iniciar novamente. Por exemplo: se vc mudar de computador ou se apagar a cópia local anterior.

---

## 4. Criar sua branch pessoal
Crie uma branch só sua:
```bash
git checkout -b aluno-seunome
git push -u origin aluno-seunome
```
⚠️ Trabalhe **sempre nessa branch**. Nunca altere a `master`.  

---

## 5. Conectar o repositório do professor (upstream)
Para receber as tarefas novas:
```bash
git remote add upstream https://github.com/awescolar/designweb.git
```

Muito importante fazer dessa forma e nunca alterar a branch master (main), pois ela vai trazer e manter todas as atividades que o professor passar.

---

## 6. Pegar novas tarefas
Quando sair coisa nova:
```bash
git fetch upstream
git checkout main
git merge upstream/master
git push origin master
```

Sempre houver novas tarefas, elas irão para branch principal. Então é sempre importante fazer esses passos. Veja que você vai baixar as atualizações do professor e atualizar no repositório pessoal.

---

## 7. Trazer as tarefas para sua branch
```bash
git checkout aluno-seunome
git merge main
```

👉 Se aparecer conflito (`<<<<<<<` e `>>>>>>>`), edite o arquivo, salve e rode:
```bash
git add .
git commit
```

---

## 8. Fazer a tarefa e entregar
Depois de resolver:
```bash
git add .
git commit -m "Tarefa X feita"
git push origin aluno-seunome
```

---

## 9. Problemas de credenciais (Windows)

Às vezes outro aluno pode ter usado o mesmo PC. Nesse caso, pode dar erro de login.  

### Ver quem está configurado
```bash
git config --list
```

### Apagar credenciais antigas
```bash
git credential-cache exit
git config --global --unset credential.helper
```

### Apagar login antigo do Windows
```bash
cmdkey /list
cmdkey /delete:git:https://github.com
```

### Configurar de novo
```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@ifrn.edu.br"
```

👉 No próximo `git push`, o VSCode abre o navegador para login no GitHub.  

---

## 10. Outros problemas comuns

1. **Esqueci em qual branch estou**  
   ```bash
   git branch
   ```
   → a com `*` é a atual.  
   Se não for sua:  
   ```bash
   git checkout aluno-seunome
   ```

2. **Erro no `git push` (upstream não configurado)**  
   ```bash
   git push -u origin aluno-seunome
   ```

3. **Merge conflict (arquivos com <<<<<<< HEAD)**  
   - Edite o arquivo → escolha a versão certa.  
   - Salve.  
   - Depois:  
     ```bash
     git add .
     git commit
     ```

4. **Esqueci de salvar o arquivo antes do commit**  
   - Salve no VSCode.  
   - Depois:  
     ```bash
     git add .
     git commit -m "mensagem"
     ```

5. **Quero cancelar mudanças no arquivo**  
   ```bash
   git checkout -- nome-do-arquivo
   ```

6. **Desfazer o último commit (mas manter os arquivos)**  
   ```bash
   git reset --soft HEAD~1
   ```

7. **Clonei no lugar errado**  
   - Feche o VSCode.  
   - Delete a pasta.  
   - Clone novamente no local certo.  

---

## 11. Dicas finais
- Trabalhe **sempre** na sua branch (`aluno-seunome`).  
- Use o **terminal do VSCode** para todos os comandos.  
- Leia os erros com calma → o Git quase sempre explica o que fazer.  
- Se não souber:  
  - Google → `git [comando] error`  
  - [docs.github.com](https://docs.github.com)  
  - [git-scm.com/docs](https://git-scm.com/docs)  

---