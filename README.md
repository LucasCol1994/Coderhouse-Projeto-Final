# Coderhouse-Projeto-Final
Este repositório tem como objetivo mostrar o projeto final exigido pela CoderHouse

# Objetivo:
O código tem como objetivo criar e manipular tabelas de um banco de dados SQLite, extrair dados da API PokeAPI, transformar e salvar esses dados em DataFrames, e finalmente, realizar merges entre esses DataFrames.

# Bibliotecas Utilizadas:

`import pandas as pd`<br/>
`import requests`<br/>
`from datetime import datetime`<br/>
`from plyer import notification`<br/>
`import sqlite3`<br/>
`import ast`<br/>

# Funções de Alerta:
**alert(nivel, base, etapa, erro=""):** Exibe notificações de alerta com base no nível de gravidade, base de dados, etapa e mensagem de erro.

# Funções de Banco de Dados:
**criar_tabelas():** Cria as tabelas do banco de dados SQLite.<br/>
**save_bd(df: pd.DataFrame, nome_tabela: str):** Salva um DataFrame no banco de dados.<br/>
**load_bd(nome_tabela):** Carrega um DataFrame do banco de dados.<br/>

# Funções de Extração da API:
**get_json_api(url):** Obtém dados da API e retorna em formato JSON.<br/>
**extract_and_save(url, table_name):** Extrai dados da API, salva em um DataFrame e armazena no banco de dados.<br/>

# Etapa de Extração:
**etapa_extracao():** Executa a extração de dados da API para pokémons, habilidades, habitats e tipos.<br/>

# Funções de Criação de Bases Específicas:
**create_pokemons_base(df_pokemons_url):** Cria a base de dados para pokémons a partir das URLs fornecidas.<br/>
**create_habilidades_base(df_habilidades_url):** Cria a base de dados para habilidades a partir das URLs fornecidas.<br/>
**create_habitats_base(df_habitat_url):** Cria a base de dados para habitats a partir das URLs fornecidas.<br/>
**create_types_base(df_types_url):** Cria a base de dados para tipos de pokémon a partir das URLs fornecidas.<br/>

# Etapa de Transformação:
**transform_and_save_pokemons(df_pokemons_full):** Realiza transformações na base de dados de pokémons e salva o resultado.<br/>
**transform_and_save_habilidades(df_habilidades_full):** Realiza transformações na base de dados de habilidades e salva o resultado.<br/>
**transform_and_save_habitats(df_habitats_full):** Realiza transformações na base de dados de habitats e salva o resultado.<br/>
**transform_and_save_type(df_types_full):** Realiza transformações na base de dados de tipos de pokémon e salva o resultado.<br/>

# Merges:
**df_merged:** Realiza merges em etapas para habitat, habilidades e pokémons.

# Observações Importantes:
    • Certificar-se de ter a biblioteca Plyer instalada para receber notificações.
    • Ajustar a lógica conforme necessário para atender a requisitos específicos.
    • O código assume que o banco de dados SQLite já está criado.
    • A documentação é extensa, mas necessária para entender o fluxo e propósito de cada parte do código.
    • Conclusão:
    • Este código realiza uma série de operações desde a criação do banco de dados até a extração, transformação e carregamento de dados da API PokeAPI. 
