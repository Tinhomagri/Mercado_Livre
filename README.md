<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>


# Cadastro de Produtos - Mercado Livre

Este projeto é uma aplicação para cadastrar produtos utilizando a API do Mercado Livre. Ele permite a criação, armazenamento e gerenciamento de produtos de forma simples e eficiente.

## Funcionalidades

- Cadastro de produtos com informações como nome, descrição, preço, quantidade e categoria.
- Upload de imagens dos produtos.
- Integração com a API do Mercado Livre para listar categorias e cadastrar produtos.

## Estrutura do Projeto

### 1. **Controllers**

- **ProdutoController**: Gerencia as operações de criação e armazenamento de produtos.

### 2. **Views**

- **create.blade.php**: Formulário para cadastrar produtos, que inclui validação e exibição de mensagens de sucesso com alertas.

### 3. **JavaScript**

- Utiliza a biblioteca SweetAlert2 para exibir mensagens de sucesso após o cadastro do produto.

## Tecnologias Utilizadas

- **PHP**: Para o desenvolvimento do backend.
- **Laravel**: Framework PHP utilizado para facilitar o desenvolvimento.
- **JavaScript**: Para manipulação de alertas e validações no frontend.
- **API do Mercado Livre**: Para obter categorias e cadastrar produtos.
- **phpMyAdmin**: Utilizado como banco de dados para armazenar as informações dos produtos.

## Como Executar o Projeto

1. Clone o repositório:
   ```bash
   git clone <URL_DO_REPOSITORIO>


2. Instale as dependências:
    ```bash
   composer install

3. Configure o arquivo `.env` com as suas credenciais de banco de dados e API.

4. Rode as migrações para criar as tabelas:
    ```bash
    php artisan migrate
    ```

5. Inicie o servidor:
    ```bash
    php artisan serve
    ```

## Banco de Dados

A aplicação usa o **phpMyAdmin** para gerenciar o banco de dados MySQL. As tabelas são criadas automaticamente utilizando as migrações do Laravel.

## 1. Controllers

- **ProdutoController**:
    - O controlador principal que gerencia as rotas de criação e listagem de produtos.
    - Faz a integração com a API do Mercado Livre para obter categorias e cadastrar produtos.
    - Após salvar o produto no banco de dados, ele realiza uma chamada à API para também cadastrar o produto no Mercado Livre.

## 2. Views

- **create.blade.php**: Página de cadastro de produtos com:
    - Campos para nome, descrição, preço, quantidade, categoria e imagem.
    - Integração com a API do Mercado Livre para selecionar categorias disponíveis.
    - Pop-up de sucesso utilizando **SweetAlert2** ao finalizar o cadastro.

## 3. JavaScript

- **SweetAlert2**:
    - Utilizado para mostrar uma notificação pop-up de sucesso após o cadastro do produto.
    - O alerta é exibido automaticamente se todos os dados forem validados e o produto for cadastrado com sucesso.

## 4. API do Mercado Livre

- O projeto faz chamadas à API do Mercado Livre para:
    - Obter a lista de categorias.
    - Enviar informações dos produtos cadastrados para o Mercado Livre.
    - É necessário um token de autenticação da API do Mercado Livre, que deve ser configurado no arquivo `.env`.

## 5. Git e GitHub

### Comandos úteis

1. Inicialize o repositório:
    ```bash
    git init
    ```

2. Adicione a URL do repositório remoto:
    ```bash
    git remote add origin git@github.com:Tinhomagri/mercado-livre.git
    ```

3. Envie o código para o GitHub:
    ```bash
    git push origin main
    ```

## Contribuição

Se deseja contribuir com este projeto, sinta-se à vontade para abrir uma issue ou um pull request.

## Licença

Este projeto está licenciado sob os termos da [MIT License](LICENSE).
