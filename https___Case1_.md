# Case 1
Imagine que você é um analista de suporte e recebe um chamado do cliente reportando
um problema na importação dos dados da Dadosfera. Você deve responder como se
estivesse interagindo com o cliente no atendimento do chamado.
O erro ocorreu nesta pipeline de coleta na Dadosfera. Sugira a alteração a ser feita no
Dataset e escreva sobre outros cuidados que nosso usuário deve ter quando carregar
dados do Google Sheets para a plataforma. Utilize a documentação da Dadosfera para
entender como baixar os logs.

Primeiramente, antes de entrar em contato com o cliente, iria estar baixando os logs de erro conforme se encontra da documentação da Dadosfera, a fim de identificar e solucionar erros, melhorar as operações, aprimorar a eficiência e entender o comportamento do usuário, já que teria informações a respeito das atividades no sistema, com registro histórico dos processos, eventos, mensagens, além de data e hora: 
-curl --request GET \
     --url https://maestro.dadosfera.ai/pipelinesV2/download-logs

Após acessar os logs e identificar os problemas, entraria em contato com o usuário:

Olá, {nome do cliente}! Sou o Dionatan, faço parte do time de Suporte da Dadosfera e estarei te auxiliando na resolução de seu problema. Verifiquei que se trata de um erro na importação de uma planilha no Google Sheets para nossa plataforma. Estarei descrevendo o passo a passo para carregar o documento de maneira rápida e segura conforme nossos procedimentos.
 
 O carregamento dos dados na Plataforma consiste basicamente em:
* Cadastrar ou escolher uma fonte de dados cadastrada;
* Definir as informações gerais da pipeline (processo em que os dados de uma origem são direcionados para um destino com ou sem processamento e transformação prévia);
* Inserir as configurações da pipeline (que variam de acordo com o tipo de fonte);
* Definir as entidades, colunas e modo de sincronização (que varia de acordo com o tipo de fonte);
* Criar micro-transformação (opcional);
* Escolher a frequência da coleta.

Em relação ao arquivo de tipo Google Sheets, seguimos os seguintes passos:
* Para iniciar a criação de uma Pipeline, basta ir no módulo Coletar, "Pipelines" aperte em "Nova Pipeline".
* Utilize uma fonte já cadastrada ou cadastre uma nova
* Atribua o Nome e uma Breve descrição para sua Pipeline.
* Parâmetros para configurações da pipeline:
Nome do campo - Link da Planilha	
Descrição - URL completa da planilha.
Exemplo - https://docs.google.com/spreadsheets/d/spreadsheetId/edit#gid=0
* Clique em "Salvar e Continuar". Obs.: Caso sua planilha tenha sido criada no Excel e carregada para o Google Drive, ela será salva com a extensão xlsx ou xls. Antes de realizar a coleta dela para a Dadosfera, certifique se o arquivo continuar nesses formatos. Caso não tenha sido realizada a mudança de extensão automaticamente, vá em: Arquivo > Salvar como Planilhas Google.
* Após inserir as credenciais você estará apto a indicar quais serão as abas a serem importadas na coleta de dados. Basta digitar o nome exato de cada aba e apertar Enter.
Ao inserir mais de uma aba, para cada aba importada será criado um dataset diferente no catálogo. Nesta versão do conector o nome das colunas não devem conter aspas duplas: ". 
* Por último, configure a frequência desejada para que sua pipeline rode. É possível escolher dentre as opções apresentadas ou inserir uma frequência customizada através de uma expressão cron. 
O fuso horário padrão utilizado na frequência é o UTC. Todos os métodos de frequência definem quando as extrações serão iniciadas. Eles não controlam por quanto tempo o trabalho de replicação será executado ou quando os dados estarão efetivamente no destino.

Pronto! Agora basta aguardar a coleta ser feita no horário e dia agendado.
Caso queira executar a pipeline imediatamente, é possível executá-la manualmente em até 30 segundos após a criação da pipeline. Vá em "Pipelines", "Lista" e "Sincronizar Pipeline".
Após alguns minutos, sua pipeline estará catalogada na aba de exploração como um Data Asset.


Por fim, estaria me despedindo e agradeçendo ao cliente pelo uso da plataforma:
Ao seguir esses passos, seu arquivo será carregado de maneira segura e eficiente, além de prevenir erros em relação à importação de arquivos. Tenha um bom proveito da plataforma! Quaisquer outros problemas, estou à disposição! 




