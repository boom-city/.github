# 💣💥 BOOM ROLEPLAY 💥💣

![Framework](https://img.shields.io/badge/Framework-QBOX-blue.svg)
![Linguagem](https://img.shields.io/badge/Linguagem-Lua-purple.svg)
![Status](https://img.shields.io/badge/Status-Em%20Desenvolvimento-yellow.svg)

Repositório oficial de desenvolvimento do servidor de GTA Roleplay **BOOM ROLEPLAY**. Este é o ponto central para todo o código-fonte, scripts, assets e configurações da nossa cidade.

---

## 📖 Sobre o Projeto

Este repositório contém todos os recursos (`resources`) e configurações necessárias para o funcionamento do servidor. Nossa base principal é a **QBOX Framework**, com diversas modificações e scripts customizados para criar uma experiência única.

### ⚠️ Atenção: Estrutura de Pastas

Por uma decisão de setup, a raiz deste repositório Git está localizada em um subdiretório do servidor: `.../txData/mri_Qbox_9A142C.base/`. Todo o desenvolvimento e comandos Git devem ser executados a partir deste diretório.

---

## 🛠️ Tecnologias Utilizadas

* **FiveM:** A plataforma base para servidores de GTA V.
* **QBOX Framework:** Nossa estrutura principal de scripts e funcionalidades.
* **Lua, JavaScript, HTML, CSS:** As linguagens de programação utilizadas nos nossos recursos.
* **Git & Git LFS:** Para controle de versão do código e gerenciamento de arquivos grandes (mapas, roupas, etc.).
* **GitHub Actions:** Para o deploy (atualização) automático do servidor após cada alteração aprovada.

---

## 🚀 Começando (Setup para Desenvolvedores)

Para começar a desenvolver, siga os passos abaixo para configurar seu ambiente local.

### Pré-requisitos

Garanta que você tenha o software abaixo instalado na sua máquina:
* [Git](https://git-scm.com/downloads)
* [Git LFS (Large File Storage)](https://git-lfs.github.com/)

Optional 
* [Github CLI](https://cli.github.com/)

### Instalação

1. clone o repositório txAdminRecipe
2. rode `make install`
3. Verifique que existe um venv `python -m venv .venv && chmod +x ./.venv/bin/activate && source ./.venv/bin/activate`
4. `make processs` ou `make process-custom DIR=path/to/folder/`

Pronto! Agora você tem uma cópia completa e funcional do projeto na sua máquina.

---

## 💻 Fluxo de Trabalho de Desenvolvimento

Para manter o projeto organizado e livre de bugs, seguimos um fluxo de trabalho rigoroso.

**A REGRA DE OURO:** ⛔ **NUNCA FAÇA PUSH DIRETAMENTE PARA A BRANCH `main`** ⛔. A `main` reflete o que está no servidor principal e deve ser sempre estável.

### Passos para Criar uma Nova Funcionalidade

1.  **Sincronize sua `main` local** com a do repositório remoto:
    ```bash
    git checkout main
    git pull origin main
    ```

2.  **Crie uma nova Branch** a partir da `main`. Use nomes descritivos com prefixos como `feature/` ou `fix/`:
    ```bash
    # Exemplo para uma nova funcionalidade
    git checkout -b feature/sistema-de-drogas

    # Exemplo para uma correção de bug
    git checkout -b fix/ajuste-no-inventario
    ```

3.  **Desenvolva e Teste:** Crie seus scripts, modifique arquivos e teste sua nova funcionalidade.

4.  **Faça "Commits" atômicos:** Salve seu progresso com frequência, usando mensagens claras que descrevem o que foi feito.
    ```bash
    # Adiciona os arquivos modificados
    git add .

    # Salva com uma mensagem
    git commit -m "feat: Adiciona a base da colheita de maconha"
    ```

5.  **Envie sua Branch** para o GitHub:
    ```bash
    git push origin feature/sistema-de-drogas
    ```

6.  **Abra um Pull Request (PR):** No site do GitHub, abra um Pull Request da sua branch para a `main`. Descreva o que você fez e por quê.

7.  **Revisão de Código:** Aguarde a aprovação de um administrador ou outro desenvolvedor. O código será revisado para garantir qualidade e evitar bugs.

8.  **Merge:** Após a aprovação, o seu PR será "mergeado" (juntado) com a `main`.

---

## 🤖 Deploy Automático

Este repositório está configurado com **GitHub Actions**. Isso significa que no momento em que um Pull Request é aprovado e mergeado na branch `main`:

1.  Uma automação é iniciada no GitHub.
2.  Ela se conecta de forma segura à VPS do servidor.
3.  Executa um `git pull` para baixar as novas alterações.
4.  Reinicia o servidor para que as novidades fiquem disponíveis para os jogadores.

**Todo o processo é 100% automático.**

---

Bem-vindo(a) à equipe de desenvolvimento do **BOOM ROLEPLAY**!

