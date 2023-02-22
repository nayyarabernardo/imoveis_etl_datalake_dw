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

## Transformação dos dados

Os dados foram transformados utilizando o PySpark e o pandas. O PySpark foi utilizado para processamento distribuído dos dados e o pandas para manipulação de dados em memória. Isso permitiu uma análise mais eficiente dos dados, reduzindo o tempo de processamento.

Algumas colunas foram criadas para uma melhor análise dos dados, como a coluna de valor por metro quadrado. Além disso, algumas colunas não necessárias, como as colunas de coordenadas, foram dropadas para simplificar a análise dos dados.

## Considerações

Este projeto demonstra como realizar um processo ETL utilizando dados imobiliários do Rio de Janeiro. As transformações realizadas nos dados permitem uma análise mais eficiente e útil das informações.

## Contribuição

Este projeto é aberto a contribuições. Se você deseja melhorar ou adicionar recursos, sinta-se à vontade para criar uma solicitação pull ou entrar em [contato](https://www.linkedin.com/in/nayyarabernardo).

## Referências

- [Documentação do Pandas](https://pandas.pydata.org/docs/)
- [Documentação do PySpark](https://spark.apache.org/docs/latest/api/python/)
- [Documentação da GCP](https://cloud.google.com/docs)
- [Documentação do MySQL](https://dev.mysql.com/doc/)
