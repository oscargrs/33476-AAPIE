### 33476-AAPIE
# Desenvolvimento de Aplicação no GITHub para interagir com API de estacionamento.

--------------------------------------------------------------------------------------------------------

É uma interface web para interagir com uma API de controle de estacionamento criada pelo professor Renato Gobet Uzum. Ela permite executar diversas operações relacionadas à entrada, saída e gerenciamento de veículos em um estacionamento.

--------------------------------------------------------------------------------------------------------

### Tecnologias usadas:
HTML + CSS → para estrutura e estilo da página.

JavaScript (Fetch API) → para fazer requisições HTTP à API.

API RESTful do estacionamento → em [http://cnms-parking-api.net.uztec.com.br/api/v1](http://cnms-parking-api.net.uztec.com.br/docs/).

--------------------------------------------------------------------------------------------------------

### Resumo das funcionalidades da aplicação:
Cada seção da interface realiza uma operação com a API:

1. **Ver Vagas Disponíveis**
Requisição: GET /slots  
Mostra quantas vagas ainda estão livres no estacionamento.

2. **Listar Veículos Ativos**
Requisição: GET /active  
Lista todos os veículos que estão estacionados no momento (ativos).

3. **Registrar Entrada**
Inputs: placa + modelo do carro.  
Requisição: POST /entry  
Adiciona um novo veículo ao estacionamento (como se ele estivesse entrando).

4. **Verificar Veículo**
Input: placa.  
Requisição: GET /check/{placa}  
Mostra os dados do veículo com a placa informada.

5. **Registrar Saída**
Input: placa.  
Requisição: PATCH /exit/{placa}  
Marca o veículo como "saiu do estacionamento", encerrando a permanência.

6. **Cancelar Registro**
Input: placa.  
Requisição: DELETE /cancel/{placa}  
Remove um veículo do sistema (como se ele nunca tivesse entrado).

7. **Ver Tempo de Permanência**
Input: placa.  
Requisição: GET /time/{placa}  
Mostra quanto tempo o veículo ficou (ou está ficando) no estacionamento.

8. **Atualizar Dados do Veículo**
Inputs: placa atual + nova placa.  
Requisição: PUT /update/{placaAntiga}  
Atualiza a placa de um veículo já registrado.

9. **Gerar Relatório Diário**
Requisição: GET /report  
Mostra um resumo do movimento do estacionamento naquele dia: entradas, saídas, tempo de permanência, etc.

--------------------------------------------------------------------------------------------------------

## Projeto desenvolvido pelo aluno: Oscar Gomes Ribeiro Silva