# 📖 Conceitos Fundamentais do GitHub Actions

Para trabalhar com GitHub Actions, é importante entender seus componentes principais:

| Termo         | Descrição                                                                                                  | Analogia com Jenkins |
| ------------- | ---------------------------------------------------------------------------------------------------------- | -------------------- |
| **Workflow**  | Um processo automatizado definido em um arquivo `.yaml`. Contém um ou mais `jobs`.                         | `Jenkinsfile`        |
| **Event**     | Um gatilho (trigger) que inicia um workflow. Ex: `push`, `pull_request`, `schedule`.                         | Triggers (SCM, etc.) |
| **Job**       | Um conjunto de `steps` que executam em um mesmo ambiente (`runner`). `Jobs` rodam em paralelo por padrão.   | `stage`              |
| **Step**      | Uma tarefa individual. Pode ser um comando (`run`) ou uma `action`.                                        | `step`               |
| **Action**    | Um comando reutilizável, como uma "biblioteca". Ex: `actions/checkout` para baixar o código.                | Plugin/Shared Library |
| **Runner**    | A máquina (servidor) que executa os `jobs`. Pode ser um ambiente do GitHub ou um auto-hospedado (`self-hosted`). | Agente/Nó Jenkins    |
