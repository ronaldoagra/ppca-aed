## O PROBLEMA DA MOCHILA APLICADO NA PRIORIZAÇÃO DE DEMANDAS DE BACKLOG DA PLATAFORMA DE IDENTIDADE DIGITAL GOV.BR

A Plataforma de Identidade Digital Gov.br, possui mais de 136 milhões de usuários, com isso, há um grande número de demandas de melhorias dos serviços e correções. 

Este grupo pesquisa métodos de otimização para auxiliar os gestores na tomada de decisões no planejamento do sprint backlog da Plataforma de Identidade Digital do Gov.br, visando entregar maior valor para o cidadão, por meio da seleção das melhorias/inovações que serão disponibilizadas nas próximas releases, de forma sistematizada e transparente.

### Métodos Estudados
- [x] Programação Inteira Mista 
- [x] Programação Linear
* Programação por Restrição

### Estrutura de arquivos
```
$DIR
├───data
│   ├───input  <-- Arquivos de entrada para realização de experimento (requisito,valor,peso)
│   └───output <-- Resultados dos experimentos
└───src <-- Arquivos executáveis
```

### Dependências
Utilizamos a biblioteca **ortools** em nossos experimentos. Para instalação em seu ambiente, siga o passo abaixo, ou visite https://developers.google.com/optimization/install:
1. python -m pip install --upgrade --user ortools

### Passo a Passo
1. Geração de dados para teste
   Executar o arquivo **$DIR/src/01-geracao-dados/ipynb** no notebook.
   
2. Verifique se foram gerados arquivos na pasta **$DIR/data/input**.   


#### Experimento múltiplas mochilas baseado no método de Programação Inteira Mista
3. Execute o arquivo **$DIR/src/02-experimento-google-ortools-mip.ipynb**, no notebook.

4. Verifique os resultados na pasta $DIR/data/output

#### Experimento múltiplas mochilas baseado no método CP-SAT
5. Execute o arquivo **$DIR/src/03-experimento-google-ortools-cpsat.ipynb**, no notebook.

6. Verifique os resultados na pasta $DIR/data/output

