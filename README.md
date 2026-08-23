# 🎓 FATEC - Desenvolvimento de Software Multiplataforma (DSM)

## Disciplina: Banco de Dados Relacional (2º Semestre)

. O foco principal é a administração, automação, segurança e otimização de bancos de dados, culminando no projeto de ecossistema para a startup fictícia de logística, a **XPTO Express**.

### 👨‍🎓 Aluno

- **Nome:** [Pedro Henrique Oliveira Silva]
- **Semestre:** [2º Semestre - 2026]

---

### 📂 Estrutura do Repositório (Por Conceitos)

#### 1. Fundamentos de Modelagem (DDL e DML)

_Pasta: `/01-fundamentos-ddl-dml`_

- `ddl_dml_setup_xpto_express.sql`: Setup completo do projeto XPTO Express, contemplando `CREATE DATABASE`, modelagem das tabelas com restrições de integridade (PK, FK, UNIQUE) e povoamento inicial (`INSERT`).

#### 2. Controle de Acesso e Governança (DCL)

_Pasta: `/02-controle-acesso-dcl`_

- `dcl_admin_politicas_acesso.sql`: Criação do usuário 'aluno_b' e políticas de `GRANT`/`REVOKE` (Visão do DBA).
- `dcl_teste_auditoria_permissoes.sql`: Testes de violação de acesso pelo usuário 'aluno_b'.
- `dcl_permissoes_usuario_suporte.sql`: (Projeto XPTO Express) Criação do usuário de suporte de TI e delegação de acessos restritos a inserções na tabela de logs.

#### 3. Abstração de Dados com Views

_Pasta: `/03-views-paineis`_

- `vw_empregado_restrito.sql`: Abstração para ocultar informações salariais de empregados.
- `vw_painel_operacional_entregas.sql`: (Projeto XPTO Express) Painel de leitura simplificado para tracking de entregas.

#### 4. Encapsulamento de Lógica (Stored Procedures)

_Pasta: `/04-stored-procedures`_

- `sp_registrar_saida_veiculo.sql`: (Projeto XPTO Express) Procedure robusta que valida a consistência do veículo e placa através de variáveis de ambiente e implementa tratamento de erro usando `SIGNAL SQLSTATE` em caso de divergências.

#### 5. Automação e Auditoria (Triggers)

_Pasta: `/05-triggers-e-auditoria`_

- `trg_regras_negocio_vendas.sql`: Conjunto de triggers (`AFTER INSERT` e `AFTER DELETE`) responsáveis pelo abatimento automático de estoque e o recálculo de pontos do programa de fidelidade do cliente.
- `trg_auditoria_exclusao_entregas.sql`: (Projeto XPTO Express) Trigger atrelada ao evento `AFTER DELETE` na tabela de entregas. Responsável por gravar um histórico detalhado da exclusão (old values) e identificar qual usuário (`CURRENT_USER()`) executou a ação na tabela de log.

#### 6. Performance e Otimização de Consultas

_Pasta: `/06-otimizacao-indices`_

- `idx_otimizacao_performance_busca.sql`: Análise do plano de execução via `EXPLAIN` e criação de índice para otimizar pesquisas textuais de nomes de clientes.
- `idx_otimizacao_placa_veiculo.sql`: (Projeto XPTO Express) Otimização estrutural baseada em `EXPLAIN` para agilizar a pesquisa pelas placas dos veículos no banco.

#### 7. Processamento de Dados (Tabelas Temporárias)

_Pasta: `/07-tabelas-temporarias`_

- `etl_limpeza_dados_tabela_temporaria.sql`: Processo de higienização de strings através de uma `TEMPORARY TABLE` e subsequente `UPDATE JOIN` para atualização na tabela matriz.
- `tmp_relatorio_fechamento_diario.sql`: (Projeto XPTO Express) Uso de tabela em memória volátil com funções de agregação matemáticas para o cálculo de frete bruto, impostos recolhidos e lucro líquido consolidado do dia.

#### 8. Rotinas de Backup e Exportação

_Pasta: `/08-backup-e-restore`_

- `bkp_dump_xpto_express_completo.sql`: (Projeto XPTO Express) Dump completo e consistente gerado pelo servidor MySQL, preservando estrutura (DDL) e registros (DML) para cenários de disaster recovery.

---

### 🛠️ Stack Tecnológico

```text
- SGBD: MySQL Server 8.0 (InnoDB Engine)
- DDL: Data Definition Language
- DML: Data Manipulation Language
- DCL: Data Control Language
- Estruturas de Programação SQL: Triggers, Stored Procedures, Views e Índices.
```
