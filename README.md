# idebr <a href='https://curso-r.github.io/idebr'><img src="https://github.com/jonates/idebr/blob/main/idebr.png?raw=true" align="right" width="120.216" height="139"/></a>

Este pacote disponibiliza datasets, com informações do IDEB - indice de desenvolvimento da educação basica, com as devidas desagregacoes e estratificacoes,ja no formato tidy, apropriado para geracao de visualizacao em ggplot2 e que podem serem utilizadas em aplicacoes no R.

Atualmente disponibiliza 3 conjuntos de dados:

1.  `ideb_brasil_fundamental_iniciais`
1.  `ideb_brasil_fundamental_finais`
1.  `ideb_brasil_ensino_medio`

O `ideb_brasil_fundamental_iniciais` contem como atributo os valores dos indicadores utilizados para o calculo do IDEB das séries iniciais (1º ao 5º ano) do ensino fundamental para o Brasil, como as taxas de aprovacoes (por serie) e as notas da prova SAEB. Conta tambem com o valor do IDEB e as metas para os anos de 2005, 2007, 2009, 2013, 2015, 2017 e 2019. Tambem estratifica essas informacoes pela rede de ensino.

O `ideb_brasil_fundamental_finais` contem como atributo os valores dos indicadores utilizados para o calculo do IDEB das séries finais (6º ao 9º ano) do ensino fundamental para o Brasil, como as taxas de aprovacoes (por serie) e as notas da prova SAEB. Conta tambem com o valor do IDEB e as metas para os anos de 2005, 2007, 2009, 2013, 2015, 2017 e 2019. Tambem estratifica essas informacoes pela rede de ensino.

O `ideb_brasil_ensino_medio` contem como atributo os valores dos indicadores utilizados para o calculo do IDEB do ensino medio para o Brasil, como as taxas de aprovacoes (por serie) e as notas da prova SAEB. Conta tambem com o valor do IDEB e as metas para os anos de 2017 e 2019. Tambem estratifica essas informacoes pela rede de ensino.

## Instalacao

``` {.r}
#Instale o pacote devtoools caso ainda não tenha instalado
#install.packages(devtools)

#instala o pacote idebr
devtools::install_github("jonates/idebr")
```

## Exemplo

``` {.r}
#carrega a base do ideb do ensino médio do Brasil
df <- idebr::ideb_brasil_ensino_medio

#Plot o gráfico do IDEB do Brasil, por ano e por rede de ensino.
library(ggplot2)
ggplot(data = df) +
  geom_point(aes(x=ano,y=IDEB,colour=rede))
```

## Roadmap

Estrato    | Fundamental - iniciais | Fundamental - finais | Ensino Medio             |
---------- | :--------------------: | :------------------: | :----------:
Brasil     | ok | ok | ok
UF         | - | - | -
Municipios | - | - | -
Escolas    | - | - | -

