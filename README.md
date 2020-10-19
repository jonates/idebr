# ideb

Este pacote disponibiliza datasets com ideb - indice de desenvolvimento da educação basica, com diversas estratificacoes, e que podem serem utilizadas em aplicacoes no R.

Atualmente disponibiliza 3 conjuntos de dados:

1. ``ideb_brasil_ensino_medio``
2. ``ideb_brasil_fundamental_iniciais``
3. ``ideb_brasil_fundamental_finais``

O ``ideb_brasil_ensino_medio`` contem como atributo os valores dos indicadores utilizados para o calculo do IDEB do ensino medio para o Brasil, como as taxas de aprovacoes (por serie) e as notas da prova SAEB. Conta tambem com o valor do IDEB e as metas para os anos de 2005, 2007, 2009, 2013, 2015, 2017 e 2019. Tambem estratifica essas informacoes pela rede de ensino.

~~~R
#Instale o pacote devtoools caso ainda não tenha instalado
#install.packages(devtools)

#instala o pacote opendatabr
devtools::install_github("jonates/opendatabr")

#carrega a base do ideb do ensino médio do Brasil
df <- opendatabr::ideb_brasil_ensino_medio

#Plot o gráfico do IDEB do Brasil, por ano e por rede de ensino.
ggplot2::ggplot(data = df) +
  geom_point(aes(x=ano,y=IDEB,colour=rede))
~~~

