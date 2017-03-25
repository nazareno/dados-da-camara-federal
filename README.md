# Dados da Câmara, reabertos

Dados organizados em csvs sobre nossos deputados federais, seus votos, seus gastos e suas proposições. Os dados existentes aqui vem de projetos como [House of Cunha](www.houseofcunha.com.br), o [Gastos da Câmara](https://github.com/nazareno/gastos-da-camara), [Dinheiro nas eleições](https://github.com/nazareno/dinheiro-nas-eleicoes2016) e [Nossos Vereadores, CG](www.vereadorescg.cc). A Câmara é excelente na provisão de dados abertos. Mas isso é feito em xml, o que é uma prova de que nada pode ser perfeito. Junto com colegas, temos tentado organizar esses dados de maneira inteligível em csvs.

## Os dados que temos

* `dados/deputados-detalhes.csv` Dados básicos sobre os 513 deputados titulares. Vem [desse endpoint](http://www.camara.leg.br/SitCamaraWS/Deputados.asmx/ObterDeputados).

* `dados/proposicoes.csv` Proposições votadas em plenário na câmara (uma ou mais vezes) desde o início de 2015. Esses dados vem [desse endpoint](http://www.camara.leg.br//SitCamaraWS/Proposicoes.asmx/ObterProposicaoPorID) na câmara.

* `dados/votacoes` Os votos de cada deputado em cada votação no plenário, [desse endpoint](http://www.camara.leg.br/SitCamaraWS/Proposicoes.asmx/ObterVotacaoProposicao).

* `dados/resumo_votacoes.csv` O resumo de cada votação segundo a câmara, mantido em uma coluna no csv. Vem do mesmo endpoint das votações, e separamos pra diminuir o tamanho dos dois arquivos.

* `dados/gastos-cota_atividade_parlamentar.csv.tgz` Dados do uso da Cota para Exercício da Atividade Parlamentar por cada um dos deputados desde o início de 2015 até o último commit desse arquivo. Os dados [vem dessa página no site da câmara](http://www2.camara.leg.br/transparencia/cota-para-exercicio-da-atividade-parlamentar/dados-abertos-cota-parlamentar). Na mesma página tem [uma explicação sobre os campos do arquivo](http://www2.camara.leg.br/transparencia/cota-para-exercicio-da-atividade-parlamentar/explicacoes-sobre-o-formato-dos-arquivos-xml) que produzimos.  

* `dados/partido-ideologias-observatorio_das_elites.csv`  Classificações dos partidos segundo o [Observatório das Elites da UTFPR](http://observatory-elites.org/). Algumas classificações podem ser polêmicas.

A lista das proposições votadas no plenário é necessária para chegar em vários dos dados acima. Ela vem [desse endpoint](http://www.camara.leg.br/SitCamaraWS/Proposicoes.asmx/ListarProposicoesVotadasEmPlenario).

## No compreendo

A Câmara tem [um glossário online](http://www2.camara.leg.br/glossario/arquivos/glossario-em-formato-pdf), e [bastante documentação online](http://www2.camara.leg.br/atividade-legislativa/processolegislativo) para ajudar a entender isso tudo.
