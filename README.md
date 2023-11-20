# CI-CD-testes
Testes de CI/CD para rodar pipelines

on:
  push:
    branches: ["main"]

## Iniciando a pipeline e definindo a branch ##
-------------------------------------------------

jobs:
  build: 
    runs-on: ubuntu-latest

## Definindo a máquina que irá rodar ##
-------------------------------------------------

steps: 
- name: Instalar npm
  run: npm install

- name: Rodar os testes
  run: npm test
  with:
    python-version: '3.x'


