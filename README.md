# 📘 ReactClienteApi – Frontend

<p align="center">
  <a href="#technologies">Tecnologias</a> •
  <a href="#features">Funcionalidades</a> •
  <a href="#structure">Estrutura</a> •
  <a href="#detailed-flow">Fluxo Detalhado</a> •
  <a href="#contact">Contato</a>
</p>

## 📖 Descrição

Aplicação **React** para gerenciamento de alunos. Permite listar, criar, editar e excluir alunos consumindo uma **API backend separada**. Utiliza **React Hooks**, **React Router** e **Axios** para comunicação com a API.

---

## 💻 Tecnologias

* React.js
* React Hooks (`useState`, `useEffect`, `useParams`, `useNavigate`)
* Axios (para requisições HTTP)
* React Router DOM (navegação entre páginas)
* HTML / CSS

---

## 🚀 Funcionalidades

✅ Listagem de alunos com filtro de busca  
✅ Criação de novos alunos  
✅ Edição de alunos existentes  
✅ Exclusão de alunos  
✅ Autenticação via JWT (armazenado no `localStorage`)  
✅ Redirecionamento automático após ações (login, salvar, editar)  

---

## 📁 Estrutura do Projeto (`src`)

```
src/
├───assets           # Imagens, ícones e recursos estáticos
├───pages
│   ├───Alunos       # Página de listagem de alunos
│   ├───Login        # Página de login
│   └───NovoAluno    # Página de criação/edição de alunos
├───services         # Configuração do Axios e chamadas à API
├───App.js           # Componente principal e roteamento
├───Global.css       # Estilos globais
├───index.js         # Entry point do React
└───routes.js        # Configuração de rotas da aplicação
```

---

## 📝 Fluxo Detalhado do Frontend

O fluxo detalhado do aplicativo inclui:

1. **Login**

   * Usuário insere credenciais na página de login.
   * Requisição POST via Axios para a API de autenticação.
   * JWT recebido armazenado no `localStorage`.
   * Redirecionamento para a página de listagem de alunos.

2. **Listagem de Alunos**

   * Página de alunos faz requisição GET para listar todos os alunos.
   * Filtro de busca é aplicado no estado local usando `useState`.

3. **Criação de Alunos**

   * Página `NovoAluno` com formulário controlado via `useState`.
   * Requisição POST via Axios para a API para criar novo aluno.
   * Após sucesso, redireciona para a lista de alunos.

4. **Edição de Alunos**

   * Página `NovoAluno` é reutilizada para edição.
   * Requisição GET com `id` do aluno para preencher o formulário.
   * Requisição PUT via Axios para atualizar os dados.
   * Redirecionamento para listagem após sucesso.

5. **Exclusão de Alunos**

   * Botão de exclusão dispara requisição DELETE via Axios.
   * Lista de alunos é atualizada imediatamente após exclusão.

---

## 📬 Contato

Autor: Paulo Santos  
GitHub: [https://github.com/paulohcarvalho07](https://github.com/paulohcarvalho07)
