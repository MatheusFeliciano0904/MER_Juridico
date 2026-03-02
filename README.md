

## Modelagem Entidade-Relacionamento (MER)

Foi realizada a modelagem conceitual do sistema utilizando a técnica de Modelo Entidade-Relacionamento (MER), com o objetivo de representar formalmente as estruturas de dados e as regras de negócio de um sistema jurídico.

A modelagem foi construída a partir da identificação das entidades do domínio, definição de seus atributos, estabelecimento de chaves primárias e especificação das cardinalidades entre os relacionamentos.

### 1. Definição das Entidades

Foram definidas como entidades principais do sistema:

* **Pessoa** – entidade central, responsável por armazenar os dados cadastrais e socioeconômicos do assistido.
* **Advogado** – representa os profissionais responsáveis pelos atendimentos jurídicos.
* **Estagiário** – representa os auxiliares responsáveis pelo atendimento e acompanhamento processual.
* **Controle_Caso** – armazena as informações relacionadas ao acompanhamento processual.
* **Disponibilidade_Advogado** – representa os horários e formatos de atendimento dos advogados.
* **Tipo_Estagiário** – classifica os estagiários conforme sua categoria.

Cada entidade foi estruturada com identificador único (chave primária), garantindo unicidade e integridade no modelo.

### 2. Entidades Dependentes

A entidade **Pessoa** foi modelada como núcleo do sistema, possuindo relacionamentos do tipo 1:N com as seguintes entidades:

* Benefício
* Tratamento
* Investimentos
* Imóveis
* Automóvel
* Endereço
* Telefones

Essas entidades armazenam informações complementares e possuem chave estrangeira referenciando Pessoa, assegurando integridade referencial.

### 3. Modelagem dos Relacionamentos

Foram definidos relacionamentos com base nas regras de negócio do sistema:

#### Relacionamentos 1:N

* Advogado → Disponibilidade_Advogado
* Tipo_Estagiário → Estagiário
* Pessoa → Entidades socioeconômicas associadas

#### Relacionamentos N:N

Os relacionamentos muitos-para-muitos foram resolvidos por meio de entidades associativas:

* Atendimento_Estagiário_realiza (Pessoa × Estagiário)
* Agenda_Adv_inscreve (Disponibilidade_Advogado × Estagiário)
* Estagiário_Controle_Caso_possui (Controle_Caso × Estagiário)

Essas entidades foram modeladas com chaves primárias compostas, garantindo a correta implementação do relacionamento no modelo lógico.

### 4. Critérios Técnicos Aplicados

A modelagem seguiu os seguintes princípios:

* Identificação de entidades fortes e dependentes
* Definição explícita de chaves primárias
* Implementação de chaves estrangeiras
* Resolução adequada de relacionamentos N:N
* Aplicação de normalização para evitar redundâncias
* Garantia de integridade referencial

O DER resultante representa de forma estruturada o fluxo de atendimento jurídico, a gestão de agenda dos advogados, o acompanhamento processual e o suporte operacional realizado por estagiários.

Se quiser, posso agora deixar ainda mais formal (nível documentação técnica de projeto) ou adaptar para ficar mais estratégico para portfólio de Analista de Dados.

