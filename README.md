# FeiraCircular — Modelagem de Banco de Dados

### Redução do desperdício de alimentos nas feiras livres de São Paulo

Projeto acadêmico desenvolvido durante a Global Solution 2026/2 da FIAP, na disciplina de Building Relational Database.

## Sobre o Projeto

O **FeiraCircular** é uma proposta de plataforma digital que busca reduzir o desperdício de alimentos nas feiras livres de São Paulo, conectando feirantes, consumidores e organizações sociais.

Segundo uma reportagem do [Jornal da USP](https://jornal.usp.br/ciencias/ciencias-ambientais/toneladas-de-alimentos-das-feiras-de-sp-vao-para-o-lixo/), publicada em 2018, uma pesquisa estimou que aproximadamente 33 mil toneladas de alimentos são descartadas anualmente nas feiras livres da cidade.

A solução propõe que alimentos excedentes, ainda próprios para consumo, possam ser comercializados com descontos ou destinados à doação.

Além de contribuir para a redução do desperdício, o projeto busca ajudar os feirantes a recuperar parte da renda que seria perdida com produtos não vendidos.

## Objetivos

- Reduzir o desperdício de alimentos nas feiras livres.
- Permitir a comercialização de excedentes com preços reduzidos.
- Facilitar doações para organizações sociais.
- Conectar feirantes, consumidores e instituições.
- Organizar o registro de ofertas, reservas e doações.
- Estruturar um banco de dados para apoiar o desenvolvimento futuro da plataforma.

## Tecnologias Utilizadas

- Oracle SQL Developer Data Modeler
- Modelagem conceitual de banco de dados
- Modelagem lógica relacional
- Diagrama Entidade-Relacionamento (DER)
- Conceitos de bancos de dados relacionais

## Estrutura do Banco de Dados

A modelagem foi desenvolvida com oito entidades principais:

| Entidade | Responsabilidade |
|---|---|
| USUARIO | Cadastro dos usuários da plataforma |
| FEIRANTE | Informações dos comerciantes e suas barracas |
| FEIRA | Cadastro e localização das feiras livres |
| ALIMENTO | Identificação e classificação dos alimentos |
| OFERTA | Registro dos produtos disponíveis para venda ou doação |
| RESERVA | Controle das reservas realizadas pelos usuários |
| ORGANIZACAO_SOCIAL | Cadastro das instituições participantes |
| DOACAO | Registro e acompanhamento das solicitações de doação |

## Relacionamentos

O banco de dados utiliza relacionamentos entre as entidades para garantir a organização e a integridade das informações.

Entre os principais relacionamentos estão:

- USUARIO — FEIRANTE: associação individual e opcional para o usuário.
- FEIRA — FEIRANTE: uma feira pode possuir vários feirantes.
- FEIRANTE — OFERTA: um feirante pode cadastrar várias ofertas.
- ALIMENTO — OFERTA: um alimento pode aparecer em diferentes ofertas.
- USUARIO — RESERVA: um usuário pode realizar várias reservas.
- OFERTA — RESERVA: uma oferta pode receber várias reservas.
- OFERTA — DOACAO: uma oferta pode originar várias solicitações de doação.
- ORGANIZACAO_SOCIAL — DOACAO: uma organização pode solicitar várias doações.

## Regras de Negócio e Integridade

Foram definidas 18 regras de negócio para orientar o funcionamento da solução.

A modelagem contempla:

- Chaves primárias (PK) e estrangeiras (FK).
- Restrições `NOT NULL` para campos obrigatórios.
- Restrições `UNIQUE` para evitar registros duplicados.
- Restrições `CHECK` para validar quantidades e valores.
- Controle de estados das reservas e doações.
- Relacionamentos que preservam a integridade referencial.

Algumas validações, como a disponibilidade de estoque antes de confirmar reservas, estão previstas para uma futura implementação da aplicação.

## Modelos Desenvolvidos

**Modelo Conceitual (DER)**

Representa as oito entidades do sistema, seus atributos e relacionamentos.

**Modelo Lógico Relacional**

Apresenta a estrutura das tabelas, os tipos de dados, as chaves primárias e estrangeiras e as restrições de integridade.

Os diagramas estão disponíveis na documentação do projeto.

## Como Abrir o Projeto

1. Baixe o arquivo ZIP disponibilizado neste repositório.
2. Extraia seu conteúdo.
3. Abra o Oracle SQL Developer Data Modeler.
4. Selecione `File > Open`.
5. Localize e abra o arquivo `.dmd` do projeto.
6. Consulte os modelos conceitual e relacional.

## Impacto e Proposta de Valor

O FeiraCircular busca gerar benefícios para diferentes participantes:

**Feirantes:** possibilidade de recuperar parte do valor investido em alimentos que não seriam comercializados.

**Consumidores:** acesso a alimentos com preços reduzidos.

**Organizações sociais:** acesso facilitado a alimentos destinados à doação.

**Meio ambiente:** redução do descarte desnecessário de alimentos.

A proposta está alinhada aos Objetivos de Desenvolvimento Sustentável (ODS) 2, 11 e 12 da ONU.

## Status do Projeto

Modelagem conceitual e lógica relacional desenvolvidas no Oracle SQL Developer Data Modeler.

A implementação da plataforma digital, suas interfaces e funcionalidades operacionais são possibilidades de desenvolvimento futuro.

## Contexto Acadêmico

**Instituição:** FIAP — Faculdade de Informática e Administração Paulista

**Projeto:** Global Solution 2026/2 — CitizenTech

**Disciplina:** Building Relational Database

**Equipe:** Grupo Bem Coletivo

Projeto desenvolvido em equipe como parte das atividades acadêmicas do curso de Análise e Desenvolvimento de Sistemas.
