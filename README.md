# 🎓 FATEC - Desenvolvimento de Software Multiplataforma (DSM)
## Disciplina: Banco de Dados Relacional (2º Semestre)

### 👨‍🎓 Aluno

- **Nome:** [Pedro Henrique Oliveira Silva]
- **Semestre:** [2º Semestre - 2026]

---

## 🚀 Competências Técnicas Desenvolvida

- Aplicação prática de conceitos no desenvolvimento de um ecossistema corporativo para a startup de logística XPTO Express.

| Módulo / Área | Competência Técnica Desenvolvida | Principais Recursos / Comandos MySQL |
| :--- | :--- | :--- |
| **1. Modelagem (DDL/DML)** | Projeto de esquemas relacionais normalizados e garantia de integridade referencial entre entidades. | `CREATE DATABASE`, `PRIMARY KEY`, `FOREIGN KEY`, `UNIQUE`, `INSERT` |
| **2. Governança (DCL)** | Gestão de perfis de acesso e aplicação do princípio do privilégio mínimo na segurança da informação. | `GRANT`, `REVOKE`, Gerenciamento de Usuários |
| **3. Abstração (Views)** | Simplificação de consultas complexas e blindagem de dados sensíveis de perfis não autorizados. | `CREATE VIEW` |
| **4. Lógica Procedural (Procedures)** | Encapsulamento de rotinas operacionais, regras de negócio e tratamento de exceções transacionais. | `CREATE PROCEDURE`, `SIGNAL SQLSTATE`, Estruturas Condicionais (`IF/ELSE`) |
| **5. Automação & Auditoria (Triggers)** | Gatilhos acoplados a eventos para automação de fluxos e rastreabilidade detalhada de logs. | `AFTER INSERT`, `AFTER DELETE`, `NEW.`, `OLD.`, `CURRENT_USER()` |
| **6. Performance (Índices)** | Diagnóstico de gargalos em planos de execução e tunning para otimização de buscas. | `EXPLAIN`, `EXPLAIN ANALYZE`, `CREATE INDEX` |
| **7. ETL & Processamento Volátil** | Higienização de strings e processamento analítico em memória para relatórios gerenciais. | `TEMPORARY TABLE`, `UPDATE JOIN`, Funções de Agregação (`SUM`) |
| **8. Backup & Restore** | Geração e exportação de dumps transacionais consolidados para recuperação de desastres. | MySQL Server Dump |

---

## 📂 Organização do Repositório (Mapeamento de Conceitos)

Os scripts encontram-se estruturados em diretórios temáticos:

- **`/01-fundamentos-ddl-dml`**: Setup inicial, criação de tabelas e cargas de dados.
- **`/02-controle-acesso-dcl`**: Gestão de perfis e governança de segurança de usuários.
- **`/03-views-paineis`**: Abstrações para painéis operacionais e proteção de dados.
- **`/04-stored-procedures`**: Lógica transacional encapsulada com tratamento de erros.
- **`/05-triggers-e-auditoria`**: Gatilhos para automações de negócio e logs de auditoria.
- **`/06-otimizacao-indices`**: Investigação de planos de execução e tunning com índices.
- **`/07-tabelas-temporarias`**: Processamentos analíticos em memória e higienização (ETL).
- **`/08-backup-e-restore`**: Dump estrutural e de dados da XPTO Express.

---

### 🛠️ Stack Tecnológico
```text
- SGBD: MySQL Server 8.0 (Engine InnoDB)
- Linguagens/Padrões: SQL (DDL, DML, DCL), Stored Procedures, Triggers, Views e Índices B-Tree.
