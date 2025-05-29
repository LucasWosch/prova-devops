 - DOCKERFILE - API PRODUTOS
    O dockerfile da api-produtos copia o index inicializa o ambiente Node e instala a biblioteca express, na porta 3001

 - DOCKERFILE - API PEDIDOS
    O dockerfile da api-pedidos copia o app inicializa o ambiente Python e instala as bibliotecas flask mysql-connector-python redis requests, na porta 3002

 - DOCKERFILE - API PAGAMENTOS
    O dockerfile da api-pagamentos copia o index e roda um servidor na porta 3003

 - DOCKERCOMPOSE
    Primeiro setamos a versão do dockercompose, depois definimos os 5 serviços que serão criados. Produtos (products) rodando na porta 3001. Pedidos (orders) rodando na porta 3002, e estou setando uma dependência com os serviços products, redis e db. Pagamentos (payments) rodando na porta 3003 e dependendo do serviço orders. O redis rodando na porta 6379, e o DB onde eu seto a senha e o nome do banco de dados rodando na porta 3306. Além disso todos os serviços estão configurados para utilizarem a mesma rede (network) ecommerce-net.
    Por fim eu defino a rede (network) Ecommerce-net.

