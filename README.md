# Projeto ETL: Dados Imobiliários do Rio de Janeiro

Este projeto consiste em extrair dados imobiliários do Rio de Janeiro de um bucket na GCP em formato JSON e Excel, utilizando as bibliotecas Pandas e PySpark para tratamento e transformação dos dados, e finalmente carregando o dataframe tratado em um bucket GCP e em um banco de dados MySQL.
Dados

## Índice

- [Sobre os Dados](#sobre-os-dados)
- [Transformação dos Dados](#transformação-dos-dados)
- [Considerações](#considerações)
- [Contribuição](#contribuição)
- [Referências](#referências)

## Sobre os Dados

Os dados imobiliários do Rio de Janeiro contêm as seguintes colunas:

- imovel_tipos_propriedade: Tipo de propriedade do imóvel.
- imovel_endereco_bairro: Bairro onde o imóvel está localizado.
- imovel_endereco_localizacao_type: Tipo de localização do imóvel.
- imovel_endereco_localizacao_coordinates: Coordenadas geográficas da localização do imóvel.
- imovel_vagasGaragem: Número de vagas de garagem do imóvel.
- imovel_area: Área do imóvel em metros quadrados.
- imovel_caracteristicas_propriedade: Características do imóvel.
- imovel_caracteristicas_condominio: Características do condomínio.
- imovel_caracteristicas_entorno: Características do entorno do imóvel.
- anuncio_tipos_publicacao: Tipo de publicação do anúncio.
- anuncio_tipos_listagem: Tipo de listagem do anúncio.
- anuncio_valores_venda: Valor de venda do imóvel.
- anuncio_valores_aluguel: Valor de aluguel do imóvel.
- anuncio_valores_condominio: Valor do condomínio do imóvel.
- anuncio_valores_iptu: Valor do IPTU do imóvel.
- anuncio_descricao: Descrição do anúncio.

## Transformação dos Dados

Foram realizadas as seguintes transformações nos dados:

- Foi criada a coluna valor_m2 com o valor do metro quadrado do imóvel.
- A coluna de coordenadas imovel_endereco_localizacao_coordinates foi dropada, pois não era necessária para análise.
- O dataframe tratado foi carregado em um bucket GCP e em um banco de dados MySQL utilizando a função to_sql.

## Considerações

Este projeto demonstra como realizar um processo ETL utilizando dados imobiliários do Rio de Janeiro. As transformações realizadas nos dados permitem uma análise mais eficiente e útil das informações.

## Referências

- [Documentação do Pandas](https://pandas.pydata.org/docs/)
- [Documentação do PySpark](https://spark.apache.org/docs/latest/api/python/)
- [Documentação da GCP](https://cloud.google.com/docs)
- [Documentação do MySQL](https://dev.mysql.com/doc/)