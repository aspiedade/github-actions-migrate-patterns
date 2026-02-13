# Migração: Stash/Jenkins para GitHub/GitHub Actions

## 🎯 Objetivo

Este repositório serve como um tutorial centralizado, contendo toda a informação necessária, padrões a serem adotados e exemplos práticos para auxiliar os times nessa transição. O objetivo é garantir que as migrações sejam feitas de forma padronizada, segura e eficiente.

## 🚀 Começando a Migração

Migrar um pipeline envolve traduzir a lógica do `Jenkinsfile` para um workflow do GitHub Actions. Siga os passos abaixo:

1. **Mapeamento para o GitHub Actions:**
    *   Um `Jenkinsfile` corresponde a um arquivo de workflow `.yaml`.
    *   `stages` no Jenkins geralmente se tornam `jobs` no GitHub Actions.
    *   `steps` dentro de um `stage` se tornam `steps` dentro de um `job`.
2. **Criação do Workflow:** Use um dos nossos exemplos pré-configurados na pasta [`/examples`](./examples) como ponto de partida.
3. **Configuração de Gatilhos (Triggers):** Defina quando seu workflow deve rodar usando a chave `on` (ex: em push para a `main`, em um pull request, etc.).
4. **Gerenciamento de Secrets:** Migre as credenciais do Jenkins para os **Secrets** do repositório ou da organização no GitHub. Veja nosso guia em: [Secrets](./docs/gerenciamento_de_secrets.md).

## 📚 Documentação e Padrões

Para garantir a consistência, criamos documentos que detalham os padrões que devem ser seguidos.

| Documento                                                             | Descrição                                                                          |
|-----------------------------------------------------------------------| ---------------------------------------------------------------------------------- |
| 📖 [**Conceitos Fundamentais**](./docs/conceitos_fundamentais.md)     | Uma explicação sobre os principais componentes do GitHub Actions.                  |
| 🏷️ [**Setup Inicial**](docs/setup_inicial.md)             | Como nomear workflows, jobs e steps para manter a organização.                     |
| 🔑 [**Gerenciamento de Secrets**](./docs/gerenciamento_de_secrets.md) | Boas práticas para armazenar e utilizar credenciais e chaves de forma segura.     |

## ✨ Exemplos Práticos

Na pasta [`/examples`](./examples), você encontrará arquivos `.yaml` prontos para serem usados como base para seus workflows.

*   [`deploy-cloud-function.yaml`](./examples/ci-cd.yaml): Workflow básico que compila e testa uma function.

## 🔗 Links Úteis

Para quem deseja se aprofundar, a documentação oficial do GitHub é o melhor lugar.

*   [Documentação oficial do GitHub Actions](https://docs.github.com/pt/actions)
*   [Guia de sintaxe para workflows](https://docs.github.com/pt/actions/using-workflows/workflow-syntax-for-github-actions)
*   [Marketplace de Actions](https://github.com/marketplace?type=actions) (para encontrar actions prontas)

---
*Este documento é mantido pelo time Caribe. Em caso de dúvidas, ou informações deprecadas , abra uma issue neste repositório.*
