Objetivo da Atividade  
Este projeto faz parte da disciplina IBD-016 – Banco de Dados Não Relacional, ministrada pelo Prof. Anderson Silva Vanin no curso de Desenvolvimento de Software Multiplataforma. O objetivo principal é construir e analisar uma base de dados no MongoDB utilizando a integração com o Google Colab e Python. A atividade exige que o aluno crie um banco de dados com informações coletadas de uma API pública, realize operações de inserção, consulta, atualização e exclusão e documente todo o processo.

Tema Escolhido 
Para esta atividade, escolhi o tema Pokémon. Utilizei a PokéAPI para coletar dados sobre vários Pokémon e armazená-los no MongoDB Atlas. Os dados coletados incluem informações como nome, altura, peso, tipos, habilidades e estatísticas dos Pokémon.

Estrutura do Projeto 🏗
O projeto está estruturado da seguinte forma:

Coleta e Estruturação dos Dados: Dados de Pokémon são coletados da PokéAPI.
Configuração do MongoDB Atlas: Configuração de um banco de dados no MongoDB Atlas para armazenar os dados coletados.
Desenvolvimento no Google Colab: Código Python para inserir, consultar, atualizar e excluir dados no MongoDB.
Coleta e Estruturação dos Dados 📊
Para coletar os dados dos Pokémon, utilizei a PokéAPI, uma API pública que fornece informações sobre Pokémon. A coleta foi feita de forma automatizada, utilizando os IDs de alguns Pokémon populares, como Bulbasaur, Charmander, Squirtle, Pikachu e Mew.

Os dados coletados incluem as seguintes informações:

id: Identificador único do Pokémon
name: Nome do Pokémon
height: Altura do Pokémon
weight: Peso do Pokémon
types: Tipos do Pokémon (ex.: "fire", "water")
abilities: Habilidades do Pokémon
stats: Estatísticas do Pokémon (ex.: "attack", "defense")
sprites: Imagens do Pokémon
Esses dados foram estruturados como documentos JSON para serem inseridos no banco de dados MongoDB.

Configuração do MongoDB Atlas 🗄
Para armazenar os dados, criei um cluster gratuito no MongoDB Atlas e configurei uma base de dados chamada pokemon_database com uma coleção chamada pokemon.

Criação do Cluster: No MongoDB Atlas, criei um cluster gratuito.
Criação do Banco de Dados e Coleção: Criei a base de dados pokemon_database e a coleção pokemon para armazenar os dados coletados.
Após configurar o MongoDB Atlas, obtive a string de conexão para conectar a aplicação Python (via Google Colab) ao banco de dados.

Desenvolvimento no Google Colab
Utilizei o Google Colab para desenvolver o código em Python que realiza as operações no MongoDB. O código foi organizado em células e possui explicações detalhadas em Markdown para facilitar o entendimento.

As principais operações realizadas são:

Inserção de Dados: Os dados dos Pokémon são inseridos na coleção pokemon do MongoDB.
Consultas: São feitas consultas para filtrar dados, como buscar Pokémon por tipo ou por nome.
Atualizações: É possível atualizar informações de Pokémon, como altura ou adicionar novos campos.
Exclusões: Também há operações para excluir Pokémon específicos ou Pokémon de um tipo específico.
O código usa a biblioteca pymongo para interagir com o MongoDB Atlas e a biblioteca requests para consumir a PokéAPI.

Documentação 📚
O notebook no Google Colab está completamente documentado com explicações detalhadas sobre cada etapa. Além disso, cada célula de código contém comentários explicativos, tornando o processo mais fácil de entender e reproduzir. O conteúdo do notebook está dividido nas seguintes etapas:

Conexão com o MongoDB Atlas.
Coleta de dados da PokéAPI.
Inserção de dados no MongoDB.
Consultas, atualizações e exclusões no MongoDB.
Como Reproduzir o Projeto 
Para reproduzir este projeto em sua máquina local, siga os passos abaixo:

Clonar o Repositório 🖥
Clone o repositório para sua máquina local:

bash
Copiar código
git clone https://github.com/seu-usuario/Atividade_MongoDB_GoogleColab.git
Abrir o Notebook no Google Colab 
Faça upload do arquivo .ipynb no Google Colab ou acesse diretamente via GitHub.
Abra o Google Colab e faça o upload do notebook ou insira a URL do seu repositório GitHub.
Configurar a Conexão com o MongoDB Atlas 
No script, substitua a string de conexão pela sua URI de conexão fornecida pelo MongoDB Atlas.
Execute as células do notebook para inserir, consultar, atualizar e excluir dados.
Tecnologias Utilizadas 🛠
Python: Linguagem de programação usada para manipular e analisar os dados.
Google Colab: Ambiente de desenvolvimento para execução de scripts em Python.
MongoDB Atlas: Serviço de banco de dados na nuvem, usado para armazenar e gerenciar os dados.
pymongo: Biblioteca Python para interagir com o MongoDB.
requests: Biblioteca Python para realizar requisições HTTP à PokéAPI.
Estrutura de Dados 
Cada documento na coleção pokemon tem a seguinte estrutura:

json
Copiar código
{
  "id": 1,
  "name": "bulbasaur",
  "height": 7,
  "weight": 69,
  "types": ["grass", "poison"],
  "abilities": ["overgrow", "chlorophyll"],
  "stats": {
    "hp": 45,
    "attack": 49,
    "defense": 49,
    "speed": 45
  },
  "sprites": {
    "front": "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/1.png"
  }
}
