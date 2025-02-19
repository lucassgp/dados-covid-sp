# Repositório de dados sobre casos e óbitos decorrentes do COVID-19 nos municípios do Estado de São Paulo e sobre leitos e internações por Departamento Regional de Saúde

## Apresentação e dados

O SEADE mantém um painel de dados sobre casos e óbitos relacionados ao coronavírus no Estado de São Paulo a partir de dados oficiais da Secretaria de Estado da Saúde de São Paulo (SES). Os dados estão disponíveis em https://www.seade.gov.br/coronavirus/.

### Casos e óbitos 

Casos e óbitos por municípios e data: **Download dos dados de casos e óbitos**: [AQUI](https://raw.githubusercontent.com/seade-R/dados-covid-sp/master/data/dados_covid_sp.csv).

### Leitos e Internações

Leitos e internações por Departamento Regional de Saúde segundo os critérios utilizados no Plano SP.

**Série antiga (variação mensal)**: [AQUI](https://raw.githubusercontent.com/seade-R/dados-covid-sp/master/data/plano_sp_leitos_internacoes_serie_nova.csv).

**Série antiga (variação semanal)**: [AQUI](https://raw.githubusercontent.com/seade-R/dados-covid-sp/master/data/plano_sp_leitos_internacoes.csv).

**Série em uso (variaçõa semanal e Grande São Paulo unificada)**: [AQUI](https://raw.githubusercontent.com/seade-R/dados-covid-sp/master/data/plano_sp_leitos_internacoes_serie_nova_variacao_semanal.csv).

### SRAG

Hospitalizados por Síndrome Respiratória Aguda Grave (SRAG). Fonte: SIVEP-Gripe. **Download dos dados de casos de SRAG**: [AQUI](https://raw.githubusercontent.com/seade-R/dados-covid-sp/master/data/SRAG_2020.csv). Última atualização: 15/06/2020

Dicionário dos dados de hospitalizados por SRAG [AQUI](https://github.com/seade-R/dados-covid-sp/blob/master/data/dicionario_de_dados_srag_hospitalizado_atual-sivepgripe.pdf)

### Casos, óbitos e doenças pré-existentes

Casos e óbitos por doenças pré-existentes, sexo e idade. Fonte: SIVEP-Gripe. **Download dos dados de casos, óbitos e doenças pré-existentes**: [FORMATO .zip](https://raw.githubusercontent.com/seade-R/dados-covid-sp/master/data/casos_obitos_doencas_preexistentes.csv.zip).

### Casos, óbitos por raça/cor e município.

Casos e óbitos por doenças pré-existentes e município. Fonte: SIVEP-Gripe. **Download dos dados casos, óbitos por raça/cor e município**: [FORMATO .zip](https://raw.githubusercontent.com/seade-R/dados-covid-sp/master/data/casos_obitos_raca_cor.csv.zip).

## Dicionário de variáveis, fontes primárias e demais informações técnicas

### Dicionário para o arquivo de casos e óbitos

|Variável|Descrição|
|---|---|
|nome_munic| Nome do município|
|codigo_ibge| Código do município no IBGE (7 dígitos)|
|dia| Dia|
|mes| Mês|
|datahora| Data no formato YYYY-MM-DD|
|casos| Casos totais registrados até a data|
|casos_novos| Casos novos registrados na data|
|casos_pc| Casos totais por 100 mil habitantes|
|casos_mm7d| Média móvel dos últimos 7 dias dos novos casos|
|obitos| Óbitos totais registrados até a data|
|obitos_novos| Óbitos novos registrados na data|
|obitos_pc| Óbitos totais por 100 mil habitantes|
|obitos_mm7d| Média móvel dos últimos 7 dias dos novos óbitos|
|letalidade| casos / obitos|
|nome_ra| Nome da Região Administrativa|
|cod_ra| Código da Região Administrativa|
|nome_drs| Nome do Dpto. Regional de Saúde|
|cod_drs| Código do Dpto. Regional de Saúde|
|pop| População Estimada (fonte: SEADE)|
|pop60| População acima de 60 anos (fonte: SEADE)|
|area| Área do município em Km2|
|map_leg| Rótulo da legenda para mapa|
|map_leg_s| Código da legenda para mapa|
|latitude| Latitude|
|longitude| Longitude|
|semana_epidem| Semana Epidemológica|

### Dicionário para o arquivo de leitos e internações

Série antiga

|Variável|Descrição|
|---|---|
|datahora| Data no formato YYYY-MM-DD|
|nome_drs| DRS ou região da Grande São Paulo|
|pacientes_uti_mm7d| Média móvel para 7 dias do Pacientes Internados em Leitos de UTI Destinados para COVID-19 no dia|
|total_covid_uti_mm7d| Média móvel para 7 dias do Total de Leitos de UTI Destinados para COVID-19 no dia|
|ocupacao_leitos| Ocupação de leitos de UTI destinados para COVID-19 (pacientes_uti_mm7d / total_covid_uti_mm7d)|
|pop| População da DRS ou região da Grande São Paulo (Fonte: SEADE)|
|leitos_pc| Leitos Covid-19 UTI por 100 mil habitantes (total_covid_uti_mm7d / pop)|
|internacoes_7d| Número de novas internações (UTI e Enfermaria) de pacientes confirmados ou com suspeita de COVID-19 nos últimos 7 dias|
|internacoes_7d_l| Número de novas internações (UTI e Enfermaria) de pacientes confirmados ou com suspeita de COVID-19 nos 7 dias anteriores|
|internacoes_7v7| Variação no número de novas internações ((internacoes_7d - internacoes_7d_l) / internacoes_7d_l)|
|pacientes_uti_ultimo_dia| Pacientes Internados em Leitos de UTI Destinados para COVID-19 no último dia|
|total_covid_uti_ultimos_dia| Total de Leitos de UTI Destinados para COVID-19 no último dia|
|ocupacao_leitos_ultimos_dia| Ocupação de leitos de UTI destinados para COVID-19 no último dia (pacientes_uti / total_covid_uti)|
|internacoes_ultimo_dia| Número de novas internações (UTI e Enfermaria) de pacientes confirmados ou com suspeita de COVID-19 no último dia|
|pacientes_enf_mm7d| Média móvel para 7 dias do Pacientes Internados em Leitos de Enfermaria Destinados para COVID-19 no dia|
|total_covid_enf_mm7d| Média móvel para 7 dias do Total de Leitos de Enfermaria Destinados para COVID-19 no dia|
|pacientes_enf_ultimo_dia| Pacientes Internados em Leitos de Enfermaria Destinados para COVID-19 no último dia|
|total_covid_enf_ultimos_dia| Total de Leitos de Enfermaria Destinados para COVID-19 no último dia|

Série nova variação semanal

|Variável|Descrição|
|---|---|
|datahora| Data no formato YYYY-MM-DD|
|nome_drs| DRS|
|pacientes_uti_mm7d| Média móvel para 7 dias do Pacientes Internados em Leitos de UTI Destinados para COVID-19 no dia|
|total_covid_uti_mm7d| Média móvel para 7 dias do Total de Leitos de UTI Destinados para COVID-19 no dia|
|ocupacao_leitos| Ocupação de leitos de UTI destinados para COVID-19 (pacientes_uti_mm7d / total_covid_uti_mm7d)|
|pop| População da DRS ou região da Grande São Paulo (Fonte: SEADE)|
|leitos_pc| Leitos Covid-19 UTI por 100 mil habitantes (total_covid_uti_mm7d / pop)|
|internacoes_7d| Número de novas internações (UTI e Enfermaria) de pacientes confirmados ou com suspeita de COVID-19 nos últimos 7 dias|
|internacoes_7d_l| Número de novas internações (UTI e Enfermaria) de pacientes confirmados ou com suspeita de COVID-19 nos 7 dias anteriores|
|internacoes_7v7| Variação no número de novas internações ((internacoes_7d - internacoes_7d_l) / internacoes_7d_l)|
|pacientes_uti_ultimo_dia| Pacientes Internados em Leitos de UTI Destinados para COVID-19 no último dia|
|total_covid_uti_ultimos_dia| Total de Leitos de UTI Destinados para COVID-19 no último dia|
|ocupacao_leitos_ultimos_dia| Ocupação de leitos de UTI destinados para COVID-19 no último dia (pacientes_uti / total_covid_uti)|
|internacoes_ultimo_dia| Número de novas internações (UTI e Enfermaria) de pacientes confirmados ou com suspeita de COVID-19 no último dia|
|pacientes_enf_mm7d| Média móvel para 7 dias do Pacientes Internados em Leitos de Enfermaria Destinados para COVID-19 no dia|
|total_covid_enf_mm7d| Média móvel para 7 dias do Total de Leitos de Enfermaria Destinados para COVID-19 no dia|
|pacientes_enf_ultimo_dia| Pacientes Internados em Leitos de Enfermaria Destinados para COVID-19 no último dia|
|total_covid_enf_ultimos_dia| Total de Leitos de Enfermaria Destinados para COVID-19 no último dia|

Série nova

|Variável|Descrição|
|---|---|
|datahora| Data no formato YYYY-MM-DD|
|nome_drs| DRS ou região da Grande São Paulo|
|pacientes_uti_mm7d| Média móvel para 7 dias do Pacientes Internados em Leitos de UTI Destinados para COVID-19 no dia|
|total_covid_uti_mm7d| Média móvel para 7 dias do Total de Leitos de UTI Destinados para COVID-19 no dia|
|ocupacao_leitos| Ocupação de leitos de UTI destinados para COVID-19 (pacientes_uti_mm7d / total_covid_uti_mm7d)|
|pop| População da DRS ou região da Grande São Paulo (Fonte: SEADE)|
|leitos_pc| Leitos Covid-19 UTI por 100 mil habitantes (total_covid_uti_mm7d / pop)|
|internacoes_28d| Número de novas internações (UTI e Enfermaria) de pacientes confirmados ou com suspeita de COVID-19 nos últimos 28 dias|
|internacoes_28d_l| Número de novas internações (UTI e Enfermaria) de pacientes confirmados ou com suspeita de COVID-19 nos 28 dias anteriores|
|internacoes_28v28| Variação no número de novas internações ((internacoes_28d - internacoes_28d_l) / internacoes_28d_l)|
|internacoes_ultimo_dia| Número de novas internações (UTI e Enfermaria) de pacientes confirmados ou com suspeita de COVID-19 no último dia|
|pacientes_enf_mm7d| Média móvel para 7 dias do Pacientes Internados em Leitos de Enfermaria Destinados para COVID-19 no dia|
|total_covid_enf_mm7d| Média móvel para 7 dias do Total de Leitos de Enfermaria Destinados para COVID-19 no dia|
|pacientes_enf_ultimo_dia| Pacientes Internados em Leitos de Enfermaria Destinados para COVID-19 no último dia|
|total_covid_enf_ultimos_dia| Total de Leitos de Enfermaria Destinados para COVID-19 no último dia|


### Dicionário para o arquivo de Casos, óbitos e doenças pré-existentes

|Variável|Descrição|
|---|---|
|codigo_ibge| Código do município no IBGE (7 dígitos) de residência do paciente|
|nome_munic| Nome do município de residência do paciente|
|idade|Idade do paciente|
|cs_sexo|Sexo do paciente|
|diagnostico_covid19|Confirmação de COVID-19|
|data_inicio_sintomas|Data de início dos sintomas|
|obito|Indica se o paciente veio a óbito por COVID-19|
|asma|Paciente apresenta esse fator de risco (asma)|
|cardiopatia|Paciente apresenta esse fator de risco (cardiopatia)|
|diabetes|Paciente apresenta esse fator de risco (diabetes)|
|doenca_hematologica|Paciente apresenta esse fator de risco (doença hematológica)|
|doenca_hepatica|Paciente apresenta esse fator de risco (doença hepática)|
|doenca_neurologica|Paciente apresenta esse fator de risco (doença neurológica)|
|doenca_renal|Paciente apresenta esse fator de risco (doença renal)|
|imunodepressao|Paciente apresenta esse fator de risco (imunodepressão)|
|obesidade|Paciente apresenta esse fator de risco (obesidade)|
|outros_fatores_de_risco|Paciente apresenta outros fatores de risco|
|pneumopatia|Paciente apresenta esse fator de risco (pneumopatia)|
|puerpera|Paciente se encontra nesse estágio (puérpera)|
|sindrome_de_down|Paciente apresenta esse fator de risco (síndrome de down)|

### Casos, óbitos por raça/cor e município

|Variável|Descrição|
|---|---|
|codigo_ibge| Código do município no IBGE (7 dígitos) de residência do paciente|
|nome_munic| Nome do município de residência do paciente|
|nome_drs| Nome do Dpto. Regional de Saúde de residência do paciente|
|obito|Indica se o paciente veio a óbito por COVID-19|
|raca_cor| Cor ou raça do paciente|
|idade|Idade do paciente|
|cs_sexo|Sexo do paciente|
|diagnostico_covid19|Confirmação de COVID-19|
|asma|Paciente apresenta esse fator de risco (asma)|
|cardiopatia|Paciente apresenta esse fator de risco (cardiopatia)|
|diabetes|Paciente apresenta esse fator de risco (diabetes)|
|doenca_hematologica|Paciente apresenta esse fator de risco (doença hematológica)|
|doenca_hepatica|Paciente apresenta esse fator de risco (doença hepática)|
|doenca_neurologica|Paciente apresenta esse fator de risco (doença neurológica)|
|doenca_renal|Paciente apresenta esse fator de risco (doença renal)|
|imunodepressao|Paciente apresenta esse fator de risco (imunodepressão)|
|obesidade|Paciente apresenta esse fator de risco (obesidade)|
|pneumopatia|Paciente apresenta esse fator de risco (pneumopatia)|
|puerpera|Paciente se encontra nesse estágio (puérpera)|
|sindrome_de_down|Paciente apresenta esse fator de risco (síndrome de down)|

### Notas

[11.06.2020] NOTA: As informações sobre leitos e internações em dias anteriores podem conter pequenas variações em novas versões publicadas em virtude de atualizações no banco de dados do Censo Covid.

[02.09.2020] NOTA: O arquivo do histórico de leitos e internações foi atualizado para se adequar aos critérios utilizados no Plano São Paulo.

#### Fontes

Casos e óbitos: SIVEP, SIMI-SP e SEADE

Leitos e internações: Censo COVID (SES) e SEADE

#### Encoding

Encoding dos arquivos: UTF-8

## Atualizações

#### [20.05.20]

A partir do dia 20.05.20, combinamos os arquivos enviados à imprensa pela Secretaria de Estado de Saúde com os dados organizados pelo Sistema de Monitoramento Inteligente (SIMI-SP), cuja fonte é também a Secretaria de Estado de Saúde.

Há novas variáveis e correções em relação às versões anteriores. As variáveis existentes desde a primeira versão e seus respectivos nomes foram mantidos.

####  [21.05.20]

A partir do dia 21.05.20, o SEADE eliminou incosistências nos dados de casos e óbitos totais acumulados, corrigindo decréscimos eventuais entre dias consecutivos.

####  [08.06.20]

A partir do dia 08.06.20, o SEADE passou a publicar as informações sobre leitos destinados ao tratamento da COVID-19 e novas internações seguindo os critérios adotados pelo Plano SP.

####  [09.08.20]

O arquivo de casos, óbitos e doenças pré-existentes será disponibilizado em formato .zip a partir desta data por ultrapassar o limite de tamanho de arquivos do github.

####  [22.08.20]

Inclusão do arquivo de casos, óbitos e raça/cor. Atualização dos dicionários das bases de casos, óbitos e doenças pré-existentes e de casos, óbitos e raça/cor. Inclusão de variáveis de taxa de ocupação de leitos e pacientes internados por DRS (média de 7 dias) no arquivo de Leitos e Internações.

####  [09.10.20]

Para acompanhar as mudanças do Plano São Paulo, adicionamos uma segunda versão do arquivo de leitos e internações com a nova regionalização da Grande São Paulo, reagrupada, e as variáveis calculadas para períodos de 28 dias.

####  [06.11.20]

Não houve atualização das informações de casos e óbitos no dia 06 de Novembro de 2020 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

####  [07.11.20]

Não houve atualização das informações de casos e óbitos no dia 07 de Novembro de 2020 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

####  [08.11.20]

Não houve atualização das informações de casos e óbitos no dia 08 de Novembro de 2020 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

####  [09.11.20]

Não houve atualização das informações de casos e óbitos no dia 09 de Novembro de 2020 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

####  [10.11.20]

Não houve atualização das informações de casos e óbitos no dia 09 de Novembro de 2020 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

####  [11.11.20]

A SES-SP retomou a extração de dados após normalização dos dados do sistema federal SIVEP, onde ocorre a notificação de casos graves e óbitos

Os dados foram atualizados na manhã do dia 11.11.20, após normalização do sistema de notificação do Ministério da Saúde que esteve inacessível desde a última sexta-feira (6) por problemas técnicos, segundo o governo federal.

Mais informações em [https://www.saopaulo.sp.gov.br/noticias-coronavirus/sp-registra-399-mil-obitos-e-115-milhao-casos-de-coronavirus/](https://www.saopaulo.sp.gov.br/noticias-coronavirus/sp-registra-399-mil-obitos-e-115-milhao-casos-de-coronavirus/)

####  [13.11.20]

Não houve atualização das informações de casos e óbitos no dia 09 de Novembro de 2020 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

####  [11.03.21]

Incluímos nos arquivos de leitos e internações as informações sobre pacientes, leitos e ocupação de leitos relativos a Covid-19 do útimos dia, ademais das médias móveis dos últimos 7 dias

####  [27.05.21]

Em razão de atualizações no sistema de organização de dados do Censo Covid, os indicadores sobre ocupação de leitos, pacientes e internações não foram disponibilizados hoje, 27/maio.

####  [28.05.21]

Em virtude de indisponibilidade do e-SUS Notifica, ferramenta online de registro de casos de COVID-19 do Ministério da Saúde, há uma variação atípica no número de novos casos em 28/maio.

####  [29.05.21]

Em razão de atualizações no sistema de organização de dados do Censo Covid, os indicadores sobre ocupação de leitos, pacientes e internações não foram disponibilizados hoje, 29/maio.

####  [30.05.21]

Em razão de atualizações no sistema de organização de dados do Censo Covid, os indicadores sobre ocupação de leitos, pacientes e internações não foram disponibilizados hoje, 30/maio.

####  [31.05.21]

Em razão de atualizações no sistema de organização de dados do Censo Covid, os indicadores sobre ocupação de leitos, pacientes e internações não foram disponibilizados hoje, 31/maio.

####  [01.06.21]

Em razão de atualizações no sistema de organização de dados do Censo Covid, os indicadores sobre ocupação de leitos, pacientes e internações não foram disponibilizados hoje, 01/junho.

####  [02.06.21]

Em razão de atualizações no sistema de organização de dados do Censo Covid, os indicadores sobre ocupação de leitos, pacientes e internações não foram disponibilizados hoje, 02/junho.

####  [17.07.21]

Não houve atualização das informações de casos e óbitos em 17/Julho/2021 por indisponibilidade dos dados.

####  [12.11.21]

Não houve atualização das informações de casos e óbitos em 12/Dezembro/2021 por indisponibilidade dos dados.

####  [14.11.21]

Em razão de problemas de instabilidade na rede externa do SEADE, os indicadores sobre ocupação de leitos, pacientes e internações foram disponibilizados hoje, 14/nov/21, após as 18h30.

#### [11.12.21]

Não houve atualização das informações de casos e óbitos no dias 11 de Dezembro de 2021 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

#### [12.12.21]

Não houve atualização das informações de casos e óbitos nos dias 11 e 12 de Dezembro de 2021 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [13.12.21]

Não houve atualização das informações de casos e óbitos nos dias 11, 12 e 13 de Dezembro de 2021 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [14.12.21]

Não houve atualização das informações de casos e óbitos nos dias 11, 12, 13 e 14 de Dezembro de 2021 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [15.12.21]

Não houve atualização das informações de casos e óbitos nos dias 11 a 15 de Dezembro de 2021 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [16.12.21]

Não houve atualização das informações de casos e óbitos nos dias 11 a 16 de Dezembro de 2021 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [17.12.21]

Não houve atualização das informações de casos e óbitos nos dias 11 a 17 de Dezembro de 2021 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [18.12.21]

Não houve atualização das informações de casos e óbitos nos dias 11 a 18 de Dezembro de 2021 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [19.12.21]

Não houve atualização das informações de casos e óbitos nos dias 11 a 19 de Dezembro de 2021 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [20.12.21]

Não houve atualização das informações de casos e óbitos nos dias 11 a 20 de Dezembro de 2021 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [21.12.21]

Não houve atualização das informações de casos e óbitos nos dias 11 a 21 de Dezembro de 2021 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [22.12.21]

Não houve atualização das informações de casos e óbitos nos dias 11 a 22 de Dezembro de 2021 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [23.12.21]

Não houve atualização das informações de casos e óbitos nos dias 11 a 23 de Dezembro de 2021 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [24.12.21]

Não houve atualização das informações de casos e óbitos nos dias 11 a 24 de Dezembro de 2021 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [25.12.21]

Não houve atualização das informações de casos e óbitos nos dias 11 a 25 de Dezembro de 2021 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [26.12.21]

Não houve atualização das informações de casos e óbitos nos dias 11 a 26 de Dezembro de 2021 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [27.12.21]

Não houve atualização das informações de casos e óbitos nos dias 11 a 27 de Dezembro de 2021 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [28.12.21]

Não houve atualização das informações de casos e óbitos nos dias 11 a 28 de Dezembro de 2021 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [29.12.21]

Não houve atualização das informações de casos e óbitos nos dias 11 a 29 de Dezembro de 2021 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [30.12.21]

Não houve atualização das informações de casos e óbitos nos dias 11 a 30 de Dezembro de 2021 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [31.12.21]

Não houve atualização das informações de casos e óbitos nos dias 11 a 30 de Dezembro de 2021 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [01.01.22]

Não houve atualização das informações de casos e óbitos nos dias 11 de Dezembro de 2021 a 01 de Janeiro de 2022 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [02.01.22]

Não houve atualização das informações de casos e óbitos nos dias 11 de Dezembro de 2021 a 02 de Janeiro de 2022 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

### [03.01.22]

Não houve atualização das informações de casos e óbitos nos dias 11 de Dezembro de 2021 a 03 de Janeiro de 2022 em virtude de problemas no sistema federal de notificação de dados da Covid-19.

## Informações adicionais

Atualização: diária, definida pelo horário de recebimento dos dados.

Autoria: [Fundação SEADE](https://www.seade.gov.br/)

Dúvidas, críticas e sugestões sobre os dados de casos e óbitos municipais: [https://www.seade.gov.br/contato/](https://www.seade.gov.br/contato/)

Por favor, pedimos a gentileza para que solicitações de dados não disponibilizados neste repositório sejam enviadas diretamente às fontes primárias.
