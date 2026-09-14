# Sistema de Gerenciamento de Compra de Uvas por Romaneio

## 1. Descrição do Sistema

O projeto consiste em um sistema de gerenciamento para intermediários de uvas, desenvolvido em linguagem C. O modelo de dados é baseado em um romaneio manual real, utilizado por um comprador de uva, que reúne em um único documento numerado (Destino, Data e Nº do romaneio) uma tabela com vários itens, cada linha trazendo Quantidade, Peso, Produto, Produtor, Preço Unitário e Preço Total, seguida de totais gerais, Comissão, Frete e Valor líquido a receber.

(foto do romaneio manual)

O sistema será destinado ao controle das operações realizadas entre compradores, produtores e vendedores de uvas. A aplicação permitirá registrar os dados dos produtores, cadastrar os produtos comercializados e gerar romaneios contendo informações como quantidade, peso, produto, preço unitário e preço total.

Além do registro das mercadorias, o sistema realizará automaticamente os cálculos relacionados à operação, como o valor total dos produtos, peso total, quantidade de volumes, comissão e frete, conforme as informações utilizadas no processo de comercialização. E o sistema também permitirá o registro das operações de compra e venda de uvas, possibilitando consultar os dados posteriormente e manter um histórico das movimentações realizadas.

A proposta busca solucionar problemas relacionados ao preenchimento manual dos romaneios, como erros de cálculo, dificuldade para localizar informações, perda de registros e necessidade de realizar repetidamente cálculos de valores e totais. Dessa forma, o sistema pretende tornar o processo de gerenciamento das operações de comercialização de uvas mais organizado, rápido e confiável, mantendo no formato digital as principais informações presentes no romaneio utilizado atualmente.

## 2. Fluxo de Utilização Esperado para o Sistema

2.1. Ao iniciar o programa, o usuário visualizará um menu principal com as opções:
   * `1. Cadastrar Produtor`
   * `2. Cadastrar Produto`
   * `3. Registrar Compra`
   * `4. Consultar Romaneios/Histórico`
   * `5. Listar Produtores`
   * `6. Listar Produtos`
   * `7. Sair`
