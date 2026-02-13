# 🏷️ Setup Inicial

Manter uma nomenclatura consistente é fundamental para a legibilidade e manutenção dos workflows.

### 1. Arquivos de Workflow (`.yaml`)
*   **Formato:** `[processo].yaml` (ex: `ci.yaml`, `build-e-deploy.yaml`, `verificacao-pr.yaml`).
*   **Local:** Devem ficar no diretório `.github/workflows/`.

### 2. Nome do Workflow (`name`)
*   **Formato:** Descreva o objetivo do workflow de forma clara.
*   **Exemplo:**
    ```yaml
    name: CI - Build e Testes
    ```

### 3. Nome do Job (`jobs.<job_id>`)
*   **Formato:** Use `kebab-case` (letras minúsculas separadas por hífen).
*   **Exemplo:**
    ```yaml
    jobs:
      build-e-test:
        name: Build e Teste
        ...
    ```
    *   A propriedade `name` (opcional) é o nome que aparece na UI do GitHub.

### 4. Nome do Step (`steps.name`)
*   **Formato:** Descreva a ação que o passo está executando.
*   **Exemplo:**
    ```yaml
    steps:
      - name: 1. Baixando o código do repositório
        uses: actions/checkout@v4

      - name: 2. Configurando o ambiente Java
        uses: actions/setup-java@v4
    ```
