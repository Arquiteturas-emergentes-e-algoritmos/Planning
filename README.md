# Planejamento

### Cronograma

O planejamento das atividades no contexto deste projeto de iniciação científica foi organizado em um cronograma detalhado, que busca acompanhar o desenvolvimento das diferentes fases do trabalho. A Tabela 1 apresenta as etapas previstas, incluindo os módulos investigativo, técnico e exploratório, bem como os períodos destinados à implementação de provas de conceito (POCs) e à análise dos resultados.

| **Mês**          | **Atividade**                                                                 |
|-------------------|-------------------------------------------------------------------------------|
| Setembro/2024     | Início das atividades, módulo investigativo, procurar por referências teóricas |
| Outubro/2024      | Módulo investigativo, procurar por referências teóricas                      |
| Novembro/2024     | Módulo investigativo técnico e exploratório, procurar por referências teóricas e iniciar implementação das POCs |
| Dezembro/2024     | Módulo técnico e exploratório, continuar implementação das POCs              |
| Janeiro/2025      | Modulo de escrita, inicio da escrita do relatório final                      |
| Fevereiro/2025    |                                                                               |
| Março/2025        |                                                                               |
| Abril/2025        |                                                                               |
| Maio/2025         |                                                                               |
| Junho/2025        |                                                                               |
| Julho/2025        |                                                                               |
| Agosto/2025       |                                                                               |
| Setembro/2025     |                                                                               |

_Tabela 1: Cronograma de atividades do projeto. Fonte: autor._

# Prova de Conceito

Para a implementação de um aplicativo "meta" em cada arquitetura, foi escolhida uma aplicação voltada para o gerenciamento de glicose e medicamentos, com foco em pessoas portadoras de diabetes.  

Como parte do processo de desenvolvimento, foi elaborado um backlog que descreve a aplicação em um nível mais próximo ao usuário, conforme apresentado na **Tabela 2**.

---

## Tabela 2: Backlog da aplicação para gerenciamento de glicemia e medicamentos

| Épico                     | Histórias de Usuário                                                                                                                                         | Moscow      |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| Monitoramento de Glicemia  | Eu, como usuário, gostaria de inserir dados de glicemia para que eu possa monitorar meus níveis de glicose no sangue.                                       | Must Have   |
| Monitoramento de Glicemia  | Eu, como usuário, gostaria de alterar dados de glicemia para que eu possa corrigir entradas erradas ou desatualizadas.                                     | Should Have |
| Monitoramento de Glicemia  | Eu, como usuário, gostaria de visualizar o histórico de glicemia para que eu possa acompanhar minhas leituras.                                              | Must Have   |
| Monitoramento de Glicemia  | Eu, como usuário, gostaria de remover dados de glicemia para que eu possa excluir entradas que não sejam mais necessárias.                                  | Should Have |
| Alarmes para Medicamentos  | Eu, como usuário, gostaria de cadastrar o horário dos meus medicamentos para que eu possa ser lembrado de tomá-los na hora certa.                           | Must Have   |
| Alarmes para Medicamentos  | Eu, como usuário, gostaria de remover medicamentos cadastrados ou que o sistema os exclua automaticamente após o término do prazo de uso.                  | Should Have |
| Alarmes para Medicamentos  | Eu, como usuário, gostaria de editar os horários dos meus medicamentos para que eu possa ajustar as informações conforme necessário.                        | Should Have |

Fonte: Autor.  

---

Em seguida, para aprofundar a análise da aplicação em um nível mais próximo ao sistema, foi elaborado um **diagrama de classes**, após um processo de refinamento contínuo. O diagrama, ilustrado na **Figura 4**, descreve as principais relações e estruturas internas da aplicação.  

Nele, é descrita a interação entre as classes `User`, `Glucometer` e `MedicationPlan`. A classe `MedicationPlan` mantém uma relação de **composição** com `Medication`, permitindo adicionar, remover e atualizar a medicação do paciente. Já `Glucometer` possui uma relação de **agregação** com `GlucoseTest`. Ambas as classes estão associadas a `User`.  

Destaca-se, ainda, a aplicação do **Design Pattern Observer**, que estabelece uma dependência **um-para-muitos** entre objetos. Dessa forma, sempre que um objeto sofre uma alteração em seu estado, todos os seus dependentes são automaticamente notificados e atualizados (HUNT, 2013). Nesse contexto, `User` atua como o **observador**, enquanto `Medication` é o **objeto observado**.  

---

**Figura 4**: Diagrama de classes final.  

Fonte: Autor.  

---

Finalmente, com base no diagrama de classes e no backlog, foi proposta uma **suíte de testes** com o objetivo de avaliar, por meio de métricas quantitativas, a qualidade de cada arquitetura.  

Os resultados desses testes foram utilizados como insumos para as análises realizadas no **SonarQube** ([https://www.sonarsource.com/products/sonarcloud/](https://www.sonarsource.com/products/sonarcloud/)) (SONARSOUCE, 2024).
