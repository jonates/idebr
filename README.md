# idebr <a href='https://curso-r.github.io/idebr'><img src="https://github.com/jonates/idebr/blob/main/idebr.png?raw=true" align="right" width="120.216" height="139"/></a>

Este pacote disponibiliza conjuntos de dados, com informações do IDEB - índice de desenvolvimento da educação básica, com as devidas desagregações e estratificações, já no formato tidy, apropriado para geração de visualizações em ggplot2 e que podem serem utilizados em diversas aplicações no R.

Atualmente disponibiliza 6 conjuntos de dados:

1.  `ideb_fundamental_iniciais_brasil`
1.  `ideb_fundamental_iniciais_escolas`
1.  `ideb_fundamental_finais_brasil`
1.  `ideb_fundamental_finais_escolas``
1.  `ideb_ensino_medio_brasil`
1.  `ideb_ensino_medio_escolas`

O `ideb_fundamental_iniciais_brasil` contem como atributo os valores dos indicadores utilizados para o calculo do IDEB das séries iniciais (1º ao 5º ano) do ensino fundamental para o Brasil, como as taxas de aprovacoes (por serie) e as notas da prova SAEB. Conta tambem com o valor do IDEB e as metas para os anos de 2005, 2007, 2009, 2013, 2015, 2017 e 2019. Tambem estratifica essas informacoes pela rede de ensino.

O `ideb_fundamental_iniciais_escolas` contem como atributo os valores dos indicadores utilizados para o calculo do IDEB das series iniciais (1º ao 5º ano) do ensino fundamental para as escolas do Brasil, como as taxas de aprovacoes (por serie) e as notas da prova SAEB. Conta tambem com o valor do IDEB e as metas para os anos de 2005, 2007, 2009, 2013, 2015, 2017 e 2019. Tambem estratifica essas informacoes pela rede de ensino.

O `ideb_fundamental_finais_brasil` contem como atributo os valores dos indicadores utilizados para o calculo do IDEB das séries finais (6º ao 9º ano) do ensino fundamental para o Brasil, como as taxas de aprovacoes (por serie) e as notas da prova SAEB. Conta tambem com o valor do IDEB e as metas para os anos de 2005, 2007, 2009, 2013, 2015, 2017 e 2019. Tambem estratifica essas informacoes pela rede de ensino.

O `ideb_fundamental_finais_escolas` contem como atributo os valores dos indicadores utilizados para o calculo do IDEB das series finais (6º ao 9º ano) do ensino fundamental para as escolas do Brasil, como as taxas de aprovacoes (por serie) e as notas da prova SAEB. Conta tambem com o valor do IDEB e as metas para os anos de 2005, 2007, 2009, 2013, 2015, 2017 e 2019. Tambem estratifica essas informacoes pela rede de ensino.

O `ideb_ensino_medio_brasil` contem como atributo os valores dos indicadores utilizados para o calculo do IDEB do ensino medio para o Brasil, como as taxas de aprovacoes (por serie) e as notas da prova SAEB. Conta tambem com o valor do IDEB e as metas para os anos de 2017 e 2019. Tambem estratifica essas informacoes pela rede de ensino.

O `ideb_ensino_medio_escolas` contem como atributo os valores dos indicadores utilizados para o calculo do IDEB do ensino medio para as escolas do Brasil, como as taxas de aprovacoes (por serie) e as notas da prova SAEB. Conta tambem com o valor do IDEB e as metas para os anos de 2017 e 2019. Tambem estratifica essas informacoes pela rede de ensino.

## Instalacao

``` {.r}
#Instale o pacote devtoools caso ainda não tenha instalado
#install.packages(devtools)

#instala o pacote idebr
devtools::install_github("jonates/idebr")
```
## Instalacao
Apos a instalacao do pacote `idebr` para carregar um conjunto de dados basta digitar no script `idebr::nomedodataset`. Caso esteja no RStudio, basta digitar `ideb::` e apertar a tecla `tab` que o autocompletar do RStudio vai mostrar todos os conjuntos de dados disponiveis no pacote `idebr` para que voce possa escolher, conforme imagem abaixo:

<img src="https://raw.githubusercontent.com/jonates/idebr/main/carregando_dados.png"/>

## Exemplo 1

``` {.r}
#carrega a base do ideb do ensino médio do Brasil
df <- idebr::ideb_brasil_ensino_medio

#Plot o gráfico do IDEB do Brasil, por ano e por rede de ensino.
library(ggplot2)
ggplot(data = df) +
  geom_point(aes(x=ano,y=ideb,colour=rede))
```
<img src="https://raw.githubusercontent.com/jonates/idebr/main/diagrama_dispersao_Brasil_EM.png"/>


``` {.r}
```

## Roadmap

Estrato    | Fundamental - iniciais | Fundamental - finais | Ensino Medio             |
---------- | :--------------------: | :------------------: | :----------:
Brasil     | ok | ok | ok
Regioes    | - | - | -
UF         | - | - | -
Municipios | - | - | -
Escolas    | ok | ok | ok

