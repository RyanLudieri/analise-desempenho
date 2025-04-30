# analise-desempenho
Simulador de Fila M/M/1 com Lei de Little
-----------------------------------------

Este programa simula uma fila do tipo M/M/1, onde chegadas e atendimentos seguem uma distribuição exponencial. 
O objetivo é analisar o desempenho do sistema e verificar a Lei de Little com diferentes níveis de ocupação.

Como funciona
-------------
A simulação gera eventos de chegada, saída e medição. A cada 100 unidades de tempo, são calculados:

- Ocupação do servidor
- E[N]: número médio de clientes no sistema
- E[W]: tempo médio de permanência no sistema
- Lambda (λ): taxa média de chegada
- Erro da Lei de Little: E[N] - λ * E[W]

Como compilar e executar
------------------------
1. Compile o código com:
   gcc simulacao.c -lm -o simulacao

2. Execute com:
   ./simulacao

Arquivos gerados
----------------
A simulação gera 4 arquivos com os resultados, um para cada nível de ocupação:

- arquivo85  → Ocupação de 85%
- arquivo90  → Ocupação de 90%
- arquivo95  → Ocupação de 95%
- arquivo99  → Ocupação de 99%

Cada linha dos arquivos contém:
[ocupação] [E[N]] [E[W]] [lambda] [erro de Little]

Saída exibida no terminal
--------------------------
Após cada simulação, são exibidas as seguintes informações:

- Maior tamanho da fila atingido
- Ocupação do servidor
- E[N]
- E[W]
- Erro da Lei de Little
- Tempo total da simulação

Autor
-----
Trabalho desenvolvido para a disciplina de Análise de Desempenho de Sistemas.
