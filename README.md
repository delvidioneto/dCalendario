
# dCalendarios com Linguagem M

Esse código gera a dCalendários com a Linguagem M.

O diferencial deste código é que já calcula os dias uteis da baixa de dias que são colocadas no parametro para criar o calendário.
 Para criar os dias uteis utilizei a Fórmula de Gauss para o calculo dos feriados advindo da páscoa, os demais demais feriados por serem datas fixar são marcados a mão.

  

## Como utilizar o código?
  

Na variável Fonte, onde é criado a listas, coloque o range de data que deseja, no caso abaixo, será criado o calendário de 01/01/2022 até o dia 31/12/2024.

      Fonte = {Number.From(#date(2022,1,1))..Number.From(#date(2024,12,31))},


Dica: Caso queria utilizar o dia atual, será necessário utilizar o Data.Localnow, conforme abaixo:

    Fonte = {Number.From(#date(2022,1,1))..Number.From(DateTime.Date(DateTime.LocalNow()))}

Na linha 50 do código é ondem marca o final de semana como não util, sendo assim, caso queira utilizar o final de semana como dia util, remova a linha, ou se somente Sábado for dia util remova o WeekDay = 6.

Abaixo é a linha que deve ser alterada.


    else if WeekDay = 0 or WeekDay = 6 then 0
