# Projeto_Analise_Documento_Antifraude
Anotações do projeto de Análise de Documento Antifraude com Azure AI
Análise de Documentos Anti-Fraude com Azure AI

Modelos pré built
Introdução
A análise de documentos anti-fraude com Azure AI permite identificar e prevenir fraudes em documentos, utilizando algoritmos avançados de inteligência artificial projeto da DIO.
Configurando a Instância e Recursos

Acessar o portal do Azure e crie uma nova instância do serviço de Análise de Documentos.
Configure os recursos necessários (Resource Group), como o Armazenamento do Azure (Storage Account), onde os documentos serão armazenados para análise. Criar um conteiner de cartões (Conteiner-name-cartoes) habilitar o BLOB para Blobs anonimos. Storage-conecting-string (pega a chacve de acesso nos dois)

Criando um Analisador de Documentos
No portal do Azure, navegue até o serviço de Análise de Documentos e selecione a opção para criar um novo analisador.
Defina os parâmetros do analisador, incluindo os tipos de documentos que serão analisados e os critérios de fraude que devem ser detectados.

Carregar um conjunto de documentos de treinamento que contenham exemplos de fraudes conhecidas.
Usar o recurso de rotulagem para identificar e marcar os elementos fraudulentos nos documentos de treinamento. Treine o modelo utilizando os documentos rotulados para que ele aprenda a identificar padrões de fraude. (Dá pra fazer com cartões, documentos, faturas e muitas outras coisas)

Executando a Análise
Carregue os documentos que precisam ser analisados no Armazenamento do Azure. Execute o analisador de documentos configurado para identificar possíveis fraudes nos documentos carregados.

No VSCode

Pasta Docs - Crias as partas
SRC
Services 
 - Blob_services importar os serviços de cliente e implantar o validador de cartão de crédito.
Utils = 
 - Criar Config.py (colocar as dependencias)
 - Em arquivo app.py - instalar as bibliotecas (azure.core, azure-ai-documentinteliigence, streamlit, azure-storage-blob, python-dotenv
 - Na parta .ENV: arquivo app.py, requiments.txt e .env (onde vai colocar as chaves,põe o endpoint, subscripton_key, azure_storage_connection_string e container name)

Revisando os Resultados
Acessar os resultados da análise no portal do Azure. Revisar os documentos sinalizados como fraudulentos e verifique os detalhes fornecidos pelo analisador.

Ajustando e Melhorando o Modelo
Com base nos resultados da análise, precisar ajustar os parâmetros do modelo para melhorar a precisão.
Continuar a treinar o modelo com novos exemplos de fraudes para mantê-lo atualizado e eficaz.

Implementação e Automação
Integrar o analisador de documentos anti-fraude com seus sistemas existentes para automação contínua. Utilizar APIs do Azure para automatizar o processo de análise e resposta a fraudes detectadas.

