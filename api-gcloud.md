## 🚀 Deploy em Nuvem com Google Cloud Run

Este projeto terminou em um deploy bem-sucedido na nuvem, utilizando o **Google Cloud Run**. A experiência de levar a API do ambiente local para um serviço escalável e globalmente acessível foi um dos pontos altos da Imersão DevOps.

**A API Escolar está disponível publicamente em:**
https://api-escolar-284329672782.southamerica-east1.run.app/docs#/

### O Processo de Deploy:

O deploy no Google Cloud, que antes parecia um bicho de sete cabeças, revelou-se um processo surpreendentemente direto e poderoso:

1.  **Autenticação e Ferramentas:** Utilizamos o `gcloud CLI` para interagir com os serviços do Google Cloud diretamente do terminal, facilitando a comunicação entre nosso ambiente local e a nuvem.
2.  **Containerização e Imagens:** A API, já conteinerizada com Docker, teve sua imagem construída e enviada para o **Google Artifact Registry**, um repositório seguro para nossos artefatos Docker.
3.  **Cloud Run:** O coração do deploy foi o **Google Cloud Run**, um serviço *serverless* que simplificou a execução da nossa API. Ele cuida de toda a infraestrutura, escalando automaticamente (inclusive para zero instâncias quando não há requisições, otimizando custos!) e nos permitindo focar exclusivamente no código.
4.  **Acesso Público:** Durante o deploy, configuramos a opção de "unauthenticated invocations" (`--allow-unauthenticated`) para que a API pudesse ser acessada publicamente através de uma URL gerada automaticamente pelo Cloud Run.

Esta etapa final da imersão consolidou todo o aprendizado sobre a importância da conteinerização, da automação de CI/CD e da praticidade da nuvem. É incrível ver como, com as ferramentas certas, podemos levar nossos projetos do código à produção de forma eficiente e confiável.