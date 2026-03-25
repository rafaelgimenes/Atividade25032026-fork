Avaliação — Engenharia de Software  
Sistema Integrado de Gestão de Farmácia

Aluno: Rafael Rosalin Gimenes  
RA: 25001652  
Data: 25/03/2026  

---

## 1. Definição do MVP

Meu MVP foca no processo de venda dentro da farmácia, desde a busca do produto até finalizar a compra.

Dentro do MVP:
- Consulta de produtos
- Verificação de estoque
- Cadastro de cliente
- Registro da venda
- Geração de conta a receber (quando for a prazo)

Ficou de fora:
- Relatórios avançados
- Controle completo financeiro
- Gestão de fornecedores detalhada

Escolhi essa parte porque é a principal no dia a dia e envolve várias etapas importantes, como estoque e cliente.

---

## 2. Regras de Negócio

RN01 — O sistema não deve permitir venda de produto sem estoque disponível.  

RN02 — Toda venda deve reduzir automaticamente a quantidade do estoque.  

RN03 — Vendas a prazo devem gerar automaticamente uma conta a receber.  

RN04 — O cliente deve estar cadastrado para realizar compras a prazo.  

RN05 — Apenas usuários autorizados podem registrar vendas.  

---

## 3. Requisitos Funcionais

RF01 — O sistema deve permitir consultar produtos por nome ou código.  

RF02 — O sistema deve verificar o estoque antes de concluir a venda.  

RF03 — O sistema deve permitir cadastrar clientes.  

RF04 — O sistema deve registrar vendas.  

RF05 — O sistema deve atualizar o estoque automaticamente após venda.  

RF06 — O sistema deve emitir comprovante da venda.  

RF07 — O sistema deve permitir vendas à vista e a prazo.  

RF08 — O sistema deve gerar conta a receber para vendas a prazo.  

---

## 4. Requisitos Não Funcionais

RNF01 — O sistema deve ser simples de usar.  

RNF02 — O sistema deve responder rapidamente às consultas.  

RNF03 — O sistema deve possuir controle de acesso por login.  

RNF04 — O sistema deve estar disponível durante o horário de funcionamento.  

---

## 5. Casos de Uso

Casos de uso do sistema:

UC01 — Realizar venda  
UC02 — Consultar produto  
UC03 — Verificar estoque  
UC04 — Cadastrar cliente  
UC05 — Registrar venda  
UC06 — Emitir comprovante  
UC07 — Gerar conta a receber  
UC08 — Validar receita  
UC09 — Identificar cliente  
UC10 — Cancelar venda  

Relacionamentos:

Include:
- Realizar venda inclui Consultar produto  
- Realizar venda inclui Verificar estoque  
- Registrar venda inclui Emitir comprovante  

Extend:
- Realizar venda estende Cadastrar cliente (se não existir)  
- Realizar venda estende Gerar conta a receber (se for a prazo)  
- Realizar venda estende Validar receita (se necessário)  

(INSERIR AQUI IMAGEM DO DIAGRAMA DE CASO DE USO)

---

## 6. Documentação dos Casos de Uso

### UC01 — Realizar venda
Ator(es): Atendente  

Descrição: Processo de venda de produtos ao cliente.  

Pré-condições:
- Sistema ativo  
- Produto cadastrado  

Pós-condições:
- Venda registrada  
- Estoque atualizado  

Fluxo Principal:
1. Atendente consulta produto  
2. Sistema mostra produto  
3. Atendente informa quantidade  
4. Sistema verifica estoque  
5. Sistema registra venda  
6. Sistema emite comprovante  

Fluxos Alternativos:

FA01 — Produto sem estoque  
- Sistema informa indisponibilidade  

FA02 — Cliente não cadastrado  
- Sistema solicita cadastro  

Relacionamentos:
Include: Consultar produto, Verificar estoque  
Extend: Cadastrar cliente, Gerar conta a receber  

(DIAGRAMA DE ATIVIDADE AQUI)

---

### UC02 — Consultar produto
Ator(es): Atendente  

Descrição: Permite buscar produtos no sistema.  

Pré-condições:
- Sistema ativo  

Pós-condições:
- Produto exibido  

Fluxo Principal:
1. Atendente digita nome ou código  
2. Sistema retorna produto  

Relacionamentos:
Include: —  
Extend: —  

(DIAGRAMA AQUI)

---

### UC03 — Verificar estoque
Ator(es): Sistema  

Descrição: Verifica quantidade disponível do produto.  

Fluxo Principal:
1. Sistema consulta estoque  
2. Retorna quantidade  

---

### UC04 — Cadastrar cliente
Ator(es): Atendente  

Descrição: Cadastro de novo cliente.  

Fluxo Principal:
1. Inserir dados  
2. Salvar  

---

### UC05 — Registrar venda
Ator(es): Sistema  

Descrição: Registra venda no sistema.  

---

### UC06 — Emitir comprovante
Ator(es): Sistema  

Descrição: Gera comprovante da venda.  

---

### UC07 — Gerar conta a receber
Ator(es): Sistema  

Descrição: Gera cobrança para venda a prazo.  

---

### UC08 — Validar receita
Ator(es): Farmacêutico  

Descrição: Valida medicamentos controlados.  

---

### UC09 — Identificar cliente
Ator(es): Atendente  

Descrição: Localiza cliente no sistema.  

---

### UC10 — Cancelar venda
Ator(es): Atendente  

Descrição: Cancela uma venda realizada.  
