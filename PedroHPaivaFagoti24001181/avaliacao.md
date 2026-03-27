## Avaliação — Engenharia de Software

Sistema Integrado de Gestão de Farmácia — MVP

Aluno: Pedro Henrique de Paiva Fagoti
RA: 24001181
Data: 26/03/2026

1. Definição do MVP

Para o meu MVP, eu decidi focar na parte mais básica e essencial de uma farmácia, que é o processo de venda.

O sistema que eu pensei permite cadastrar clientes e produtos, consultar essas informações e realizar uma venda simples, já atualizando o estoque automaticamente.

## O que está dentro do MVP:

-- Cadastro de cliente
-- Cadastro de produto
-- Consulta de cliente e produto
-- Realização de venda
-- Verificação de estoque
-- Atualização do estoque
-- Emissão de comprovante simples
## O que está fora do MVP:

-- Integração com formas de pagamento (cartão, PIX, etc.)
-- Controle de fornecedores
-- Relatórios mais avançados
-- Controle de validade de medicamentos
-- Sistema de entrega
-- Por que escolhi isso:

Eu optei por deixar o sistema mais simples porque a ideia do MVP é justamente validar o funcionamento principal. Então foquei no fluxo de venda, que é o mais importante dentro de uma farmácia.

2. Regras de Negócio

RN01 -- Cliente precisa estar cadastrado
Para fazer uma compra, o cliente deve já estar no sistema.

RN02 -- Não pode vender sem estoque
O sistema não permite vender produtos que estejam sem quantidade disponível.

RN03 -- Estoque é atualizado automaticamente
Quando uma venda é feita, o sistema já diminui a quantidade do produto.

RN04 -- Produto precisa ter preço válido
Não pode cadastrar produto com preço zero ou negativo.

RN05 -- Cada produto tem um código único
Não pode ter dois produtos com o mesmo código.

RN06 -- Venda precisa ter pelo menos um item
Não é possível finalizar uma venda vazia.

3. Requisitos Funcionais

RF01 — O sistema deve permitir cadastrar cliente
RF02 — O sistema deve permitir consultar cliente
RF03 — O sistema deve permitir cadastrar produto
RF04 — O sistema deve permitir consultar produto
RF05 — O sistema deve permitir atualizar produto
RF06 — O sistema deve permitir realizar venda
RF07 — O sistema deve verificar o estoque antes da venda
RF08 — O sistema deve atualizar o estoque automaticamente
RF09 — O sistema deve emitir comprovante da venda
RF10 — O sistema deve permitir remover produto

🛡 4. Requisitos Não Funcionais

RNF01 — Desempenho
O sistema deve responder rápido, de preferência em até 2 segundos.

RNF02 — Segurança
O acesso ao sistema deve ser feito com login e senha.

RNF03 — Usabilidade
A interface deve ser simples, fácil de entender e usar.

RNF04 — Disponibilidade
O sistema deve funcionar na maior parte do tempo, sem ficar fora do ar.

RNF05 — Armazenamento de dados
Os dados devem ser salvos de forma segura.

5. Casos de Uso
Atores:
Atendente
Administrador
Casos de Uso:

UC01 — Cadastrar Cliente
<img width="324" height="312" alt="image" src="https://github.com/user-attachments/assets/8f082fe0-b55e-4952-8a95-bba94c7d53b3" />
UC02 — Consultar Cliente
<img width="301" height="257" alt="image" src="https://github.com/user-attachments/assets/f64dc6ab-4645-49bd-a0a8-82003b49b36e" />

UC03 — Cadastrar Produto
<img width="219" height="312" alt="image" src="https://github.com/user-attachments/assets/d6a6b24b-a52c-43db-806f-05d84165038d" />

UC04 — Consultar Produto
<img width="307" height="257" alt="image" src="https://github.com/user-attachments/assets/25303dd0-f901-47df-afe4-07535ddac552" />

UC05 — Atualizar Produto
<img width="233" height="367" alt="image" src="https://github.com/user-attachments/assets/9f2f2fe8-090b-4d37-9678-23fec5476b59" />

UC06 — Realizar Venda
<img width="636" height="606" alt="image" src="https://github.com/user-attachments/assets/d8700713-9eee-44c6-a986-1122b45ac2ce" />

UC07 — Verificar Estoque
<img width="286" height="257" alt="image" src="https://github.com/user-attachments/assets/72c0cd39-a99a-47d9-9239-d0cee3075f79" />

UC08 — Atualizar Estoque
<img width="231" height="367" alt="image" src="https://github.com/user-attachments/assets/41096a11-ef12-4afd-a3fa-0f4c0f711efc" />

UC09 — Emitir Comprovante
<img width="147" height="248" alt="image" src="https://github.com/user-attachments/assets/0424ad32-a880-491c-be6c-6cbce5684465" />

UC10 — Login no Sistema
<img width="324" height="312" alt="image" src="https://github.com/user-attachments/assets/3a50183f-3545-4dce-8ee0-6e4e74fa06cf" />


Relacionamentos

Include (inclui):

Realizar Venda → Verificar Estoque
Realizar Venda → Atualizar Estoque
Realizar Venda → Emitir Comprovante

Extend (estende):

Consultar Cliente → Cadastrar Cliente (caso não exista)
Consultar Produto → Cadastrar Produto (caso não exista)
Realizar Venda → Consultar Cliente
6. Documentação dos Casos de Uso
UC06 — Realizar Venda

Ator: Atendente

Descrição:
Esse caso de uso representa o processo de venda de produtos para um cliente dentro da farmácia.

Pré-condições:

Usuário precisa estar logado
Cliente precisa estar cadastrado
Produto precisa estar cadastrado

Pós-condições:

Venda registrada no sistema
Estoque atualizado
Comprovante gerado
Fluxo Principal
O atendente inicia a venda
O sistema pede o cliente
O atendente informa o cliente
O sistema pede os produtos
O atendente adiciona os produtos
O sistema verifica o estoque
O sistema calcula o valor total
O atendente confirma a venda
O sistema atualiza o estoque
O sistema gera o comprovante
Fluxos Alternativos

FA01 — Cliente não encontrado
O sistema pede para cadastrar o cliente antes de continuar.

FA02 — Estoque insuficiente
O sistema mostra uma mensagem informando que não tem quantidade suficiente.

FA03 — Cancelamento da venda
O atendente pode cancelar a venda antes de finalizar.

Relacionamentos

Inclui:

Verificar Estoque
Atualizar Estoque
Emitir Comprovante

Estende:

Consultar Cliente
Estender:

Consultar Cliente
