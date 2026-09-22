# Sistema de Gerenciamento de Compra de Uvas por Romaneio

## 1. Descrição do Sistema

O projeto consiste em um sistema de gerenciamento para intermediários de uvas, desenvolvido em linguagem C. O modelo de dados é baseado em um romaneio manual real (Figura 01), utilizado por um comprador de uva, que reúne em um único documento numerado (Destino, Data e Nº do romaneio) uma tabela com vários itens, cada linha trazendo Quantidade, Peso, Produto, Produtor, Preço Unitário e Preço Total, seguida de totais gerais, Comissão, Frete e Valor líquido a receber.

<p align="center">
Figura 01 – Romaneio manual
</p>
<p align="center">
  <img width="500" alt="Image" src="https://github.com/user-attachments/assets/25ef3f5d-1abd-4595-ab58-9d876b91de02](https://github.com/user-attachments/assets/78ba6bd2-ee89-44a3-8840-3f7d1ae20462" />
</p>

O sistema será destinado ao controle das operações realizadas entre compradores, produtores e vendedores de uvas. A aplicação permitirá registrar os dados dos produtores, cadastrar os produtos comercializados e gerar romaneios contendo informações como quantidade, peso, produto, preço unitário e preço total.

Além do registro das mercadorias, o sistema realizará automaticamente os cálculos relacionados à operação, como o valor total dos produtos, peso total, quantidade de volumes, comissão e frete, conforme as informações utilizadas no processo de comercialização. E o sistema também permitirá o registro das operações de compra e venda de uvas, possibilitando consultar os dados posteriormente e manter um histórico das movimentações realizadas.

A proposta busca solucionar problemas relacionados ao preenchimento manual dos romaneios, como erros de cálculo, dificuldade para localizar informações, perda de registros e necessidade de realizar repetidamente cálculos de valores e totais. Dessa forma, o sistema pretende tornar o processo de gerenciamento das operações de comercialização de uvas mais organizado, rápido e confiável, mantendo no formato digital as principais informações presentes no romaneio utilizado atualmente.

___


## 2. Fluxo de Utilização Esperado para o Sistema

### 2.1 Menu Principal
Ao iniciar o programa, o usuário visualizará um menu principal com as opções:
   * `1. Cadastrar Produtor`
   * `2. Cadastrar Produto`
   * `3. Registrar Compra`
   * `4. Histórico de Romaneios`
   * `5. Listar Produtores`
   * `6. Listar Produtos`
   * `7. Sair`

### 2.2 Cadastro de Produtor

Ao selecionar a opção `1`, o sistema solicitará os dados necessários para cadastrar um produtor.

Serão solicitadas informações como:

* Código do produtor;
* Nome do produtor;
* CPF/CNPJ;
* Telefone;
* Propriedade ou localidade.

Após o preenchimento, os dados serão armazenados no sistema e poderão ser utilizados posteriormente no registro dos romaneios e salvará a struct no arquivo `produtores.dat`.

### 2.3 Cadastro de Produto

Na opção `2`, o usuário poderá cadastrar as variedades de uva comercializadas.

Serão solicitadas informações como:

* Código do produto;
* Variedade da uva;
* Unidade de comercialização;
* Preço unitário.

Os produtos cadastrados poderão ser selecionados posteriormente durante o preenchimento dos romaneios e a struct será salva no arquivo `produtos.dat`.

### 2.4 Registro de Romaneio de Compra

Ao selecionar a opção `3`, o sistema iniciará o registro de um romaneio de compra.

Primeiramente, serão solicitados os dados gerais da operação:

* Número do romaneio;
* Data;
* Tipo de operação;
* Destino.

Em seguida, o usuário poderá inserir um ou mais itens no romaneio.

Para cada item serão informados:

* Quantidade de volumes;
* Peso;
* Produto;
* Preço unitário;
* Produtor.

O sistema calculará automaticamente o valor total de cada item:

Preço Total = Peso × Preço Unitário

Após o cadastro dos itens, o sistema calculará os totais do romaneio, incluindo:

* Quantidade total de volumes;
* Peso total;
* Valor total dos produtos;
* Comissão;
* Frete;
* Valor final.

O romaneio também receberá uma situação de pagamento:

* 1 - PAGO
* 2 - PENDENTE

A struct será salva no arquivo `romaneios.dat`.

### 2.5 Histórico de Romaneios
Na opção `4`, o usuário poderá consultar os romaneios registrados anteriormente. O sistema permitirá a consulta por:

* Número do romaneio;
* Produtor;
* Produto;
* Data;
* Tipo de operação – compra ou venda.

Após localizar o registro no arquivo `romaneios.dat`, exibirá seus dados e o usuário vai poder alterar sua situação de pagamento de `Pendente` para `Pago`.

### 2.6 Listagem de produtores e produtos
As opções `5` e `6` permitirão visualizar os cadastros existentes no sistema, armazenados em `produtores.dat` e `produtos.dat`.

### 2.7 Encerramento
Ao selecionar a opção `7`, o sistema encerrará a execução.

___


## 3. Fluxograma da Lógica do Sistema
<p align="center">
Figura 02 – Fluxograma
</p>
<p align="center">
  <img width="500" alt="Image" src="https://github.com/user-attachments/assets/591bc431-fee2-4336-bede-1b8393d75430" />
</p>
