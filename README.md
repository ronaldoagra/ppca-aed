## O PROBLEMA DA MOCHILA APLICADO NA PRIORIZAÇÃO DE DEMANDAS DE BACKLOG DA PLATAFORMA DE IDENTIDADE DIGITAL GOV.BR

A Plataforma de Identidade Digital Gov.br, possui mais de 136 milhões de usuários, com isso, há um grande número de demandas de melhorias dos serviços e correções. 

Este grupo pesquisa métodos de otimização para auxiliar os gestores na tomada de decisões no planejamento do sprint backlog da Plataforma de Identidade Digital do Gov.br, visando entregar maior valor para o cidadão, por meio da seleção das melhorias/inovações que serão disponibilizadas nas próximas releases, de forma sistematizada e transparente.

### Métodos Estudados
- [x] Programação Inteira Mista 
- [x] Programação por restrição
- [x] Força Bruta

### Estrutura de arquivos
```
$DIR
├───data
│   ├───input  <-- Arquivos com dados ficticios de entrada para realização de experimento (requisito,valor,peso)
│   └───output <-- Arquivos com os resultados dos experimentos (alocação dos itens de backlog nas sprints)
│   └───real   <-- Arquivo com o resultado da alocação dos itens de backlog reais
└───src <-- Códigos (Jupyter Notebooks) para a realização dos experimentos.
└───Documento de Requisitos.docx <-- Documento com a descrição dos requisitos de negócio
```

### Dependências
Utilizamos a biblioteca **ortools** em nossos experimentos. Para instalação em seu ambiente, execute o comando abaixo, ou visite https://developers.google.com/optimization/install, para ter acesso a documentação completa:

python -m pip install --upgrade --user ortools

### Passo a Passo - execução dos experimentos com geração de dados ficticios
1. Gerar os dados para teste

   Executar o arquivo **$DIR/src/01-geracao-dados/ipynb**.
   
2. Verificar se foram gerados arquivos na pasta **$DIR/data/input**.   


#### Experimento múltiplas mochilas baseado no método de Programação Inteira Mista
3. Executar o arquivo **$DIR/src/02-experimento-google-ortools-mip-dados-ficticios.ipynb**.

#### Experimento múltiplas mochilas baseado no método CP-SAT
4. Executar o arquivo **$DIR/src/03-experimento-google-ortools-cpsat-dados-ficticios.ipynb**.

#### Experimento múltiplas mochilas baseado em algoritmo de força bruta
5. Executar o arquivo **$DIR/src/04-força-bruta.ipynb**, no notebook.

6. Verificar os resultados na pasta $DIR/data/output

### Passo a Passo - execução dos experimentos com geração de dados reais
1. Verificar se o arquivo **$DIR/data/real/backlog-real-70-req.csv** está disponível.
2. Para o método MIP, executar o arquivo **$DIR/src/02-experimento-google-ortools-mip.ipynb**.
3. Para o método CP-SAT, executar o arquivo **$DIR/src/03-experimento-google-ortools-cpsat.ipynb**.
4. Verificar o resulto obtido no diretório **$DIR/data/output**.