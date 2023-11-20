# CI-CD-testes
Testes de CI/CD para rodar pipelines

# Iniciando a pipeline e definindo a branch #
on:
  push:
    branches: ["main"]


# Definindo a máquina que irá rodar #

jobs:
  build: 
    runs-on: ubuntu-latest


# Passos que irá executar #

steps: 
- name: Instalar npm
  run: npm install

- name: Rodar os testes
  run: npm test
  with:
    python-version: '3.x'


