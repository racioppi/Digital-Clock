# Projeto de Estudo: Prática de Git, GitHub e Feature Branch Workflow

Este repositório foi criado com o objetivo de praticar e consolidar o uso do Git e do GitHub em um fluxo de trabalho profissional baseado em _Feature Branch Workflow_.

## 🧠 Objetivo

- Simular o desenvolvimento de um projeto real com separação clara entre funcionalidades.
- Aprender a criar, versionar e integrar branches específicos.
- Testar deploy automático usando o **Netlify** com base no branch `main`.

---

## 📁 Estrutura do Projeto

O projeto é composto por arquivos estáticos:

- `index.html` – estrutura da página
- `style.css` – estilos visuais
- `script.js` – interatividade (básica)
- Imagem ilustrativa (`.jpg/.png`)

---

## 🧪 Fluxo de Trabalho Aplicado

### 🟢 1. `main`

Branch principal do projeto, mantido limpo e sempre pronto para deploy.

### 🌿 2. `html`

Branch criado a partir do `main` para alterações específicas no HTML.

- Criado com: `git checkout -b html main`
- Mergeado para `main` após conclusão.

### 🌿 3. `css`

Branch criado a partir do `html` (pois dependia das alterações nele) para trabalhar no CSS.

- Criado com: `git checkout -b css html`
- Mergeado para `main` após o `html`.

### 🌿 4. `js`

Branch criado a partir do `main` (já atualizado com `html` e `css`) para trabalhar no JavaScript.

- Criado com: `git checkout -b js main`
- Mergeado para `main` após finalização.

---

## 🔄 Integração e Deploy

- Todos os branches de feature foram **mergeados via Pull Request** para o `main`.
- Após cada merge, o **Netlify** fez o deploy automático da nova versão do projeto.

---

## 🧹 Limpeza Final

Após os merges, os branches `html`, `css` e `js` foram apagados:

```bash
# Deleção local
git branch -d html
git branch -d css
git branch -d js

# Deleção remota (GitHub)
git push origin --delete html
git push origin --delete css
git push origin --delete js
```
