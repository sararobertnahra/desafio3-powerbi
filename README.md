# Desafio 3 PowerBI
O objetivo desse desafio é criar uma instância na Azure para MySQL, criar o Banco de dados e integrar o PowerBI com MySQL no Azure.

No início do projeto me deparei com alguns problemas, como por exemplo, o conector mais recente não estava funcionando e, portanto, tive que utilizar uma versão menos recente do conector (8.0.28) e este funcionou. Além disso, precisei utilizar o dotnet 7.

Embora tenha conseguido conectar com utilizando o Workbench, não consegui realizar o acesso (autenticar) com a Azure.

Para simular o ambiente, utilizei o docker, sendo que o conteiner foi criado utilizando a seguinte configuração: ``docker-compose.yaml``. 

SQL executa códigos sequencialmente, então se der erro em alguma linha, ele pára a execução. Por isso, tive que excluir as linhas de drop e alter table que estavam dando problema. Adicionalmente, tive que mudificar o nome do banco alterando o ``use`` para ``use azure_company``.

Respondendo a pergunta proposta no Desafio (Questão 14):
Utilizamos o mesclar, pois estamos lidando com a combinação de conjuntos de dados ou operações. Caso estivessemos lidando com um valor de uma variável ou propriedade, então utilizaríamos o atribuir.
