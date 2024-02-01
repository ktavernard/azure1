# azure1
Desafio DIO azure

Inicialmente, acessar https://azure.microsoft.com/pt-br/free/
Entrar (botaõ no canto superior direio);
    Como eu já tinha conta feita, apeas fiz o login;
Acesar dashboard Azure Machine Learning;
Clicar no "+ Criar";
    Criar novo workspace (para projetos e equipes ML);
Assinatura: assinatura do Azure 1 (já tinha assinado uma conta gratuita);
Grupo de recursos: LABKAR-900 (é onde estarão guardadas todas as coisas criadas após esse passo);
Nome: laboratoriokar900 (deverá criar algo "específico");
Região: East US 2;
O restante desse primeiro formulário, não mexe.
Clicar no canto inferior direito em: EXAMINAR + CRIAR ;
    Se a validação estiver ok (canto superior esquerdo), pode clicar em CRIAR;
Aguardar a implementação estar concluída;
Clicar em  IR PARA O RECURSO;
Na página que abrir, logo no meio, clicar no botão: INICIAR O ESTÚDIO;
    Vai ficar carregando o workspace;
No dashboard do laboratório, irá aparecer um catálogo de modelos;
No Menu esquerdo, clicar em ML AUTOMATIZADO;
    Clicar em NOVO TRABALHO DE ML ATUMATIZADO;

Para continuar com o testa, acessar a documentação da Microsoft que se encontra no link: https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/01-machine-learning.html
    Nesse link encontramos a documentação necessária para preenchermos os devidos campos e conseguirmos dar segmento ao projeto-teste;
Nome do trabalho: mslearn-bike-automl;
Novo nome do experimento : mslearn-bike-rental;
Descrição : Aprendizado de máquina automatizado para previsão de aluguel de bicicletas;
Marcas : nenhuma;
Avançar;
Tipo de tarefa e dados:
    Selecionar tipo de tarefa: Mudar para REGRESSÃO;
Clicar em +CRIAR;
Definir o nome e o tipo do ativo de dados: alugueldebicicletas;
Descrição: dados históricos de aluguel de bicicletas;
Tipo: Tabular;
AVANÇAR;
Ao escolher uma fonte para o ativo de dados, selecione: De arquivos da Web (Crie um ativo de dados a partir de um único arquivo localizado em uma URL pública da Web);
AVANÇAR;
Insira uma URL da Web (Especifique a URL de uma página da Web pública da qual você deseja seus dados sejam recuperado);
   URL da documentação Microsoft: https://aka.ms/bike-rentals;
AVANÇAR;
Irá processar a validação do link;
    OBS.: Não mexe nas configurações;
Aguardar processamento e AVANÇAR;
Na página "Esquema", AVANÇAR;
Na página "Examinar", CRIAR;
Tipo de tarefa e dados deverá aparecer a seguinte mensagem: Êxito: Ativo de dados alugueldebicicletas criado com sucesso. A atualização das listas pode demorar alguns segundos.Clique aqui para acessar esse ativo de dados;
Clicar em ALUGUELDEBICICLETAS;
AVANÇAR;
Na configuração de tarefas, mudar a coluna de destino para: RENTALS;
Clicar em: Exibir definições de configuração adicionais;
    Ao abrir um menu adicional à direita, desmarcar as opções que estiverem marcadas;
    EM Modelos permitidos clicarm em RANDON e LIGHT;
SALVAR;
Logo abaixo, em limites:
  Máximo de testes: 3
  Máximo de testes simultâneos: 3
  Máximo de nós: 3
  Limite de pontuação da métrica: 0,085 
  Tempo limite: 15
  Tempo limite de iteração: 15
  Selecionar: Habilitar rescisão antecipada;
Tipo de validação: divisão de validação de treinamento;
  Validação de percentual de dados: 10;
  Dados de teste: Nenhum;
AVANÇAR;
Página COMPUTAÇÃO, não mexe;
AVANÇAR;
Clicar no botão azul: ENVIAR TRABALHO DETREINAMENTO

Observar o Status: em execução;
Demora aproximadamente 15 minutos;

Agora iremos para a validação;

Selecione no menu direito, um pouco mais abaixo: Nome do algoritmo;
Clique em IMPLANTAR;
Selecione SERVIÇOS DE WEB;
   Nome: prever-alugueis;
   Descrição: Prever aluguel de bicicletas;
   Tipo de computação: Instância de Contêiner do Azure;
   Habilitar autenticação;
IMPLANTAR;
Aparecerá a mensagem: "Êxito: A implantação de modelo foi disparada com êxito";

No Menu esquerdo, clicar em MODELOS;
Clica no modelo que aparece;
Selecione DETALHES;
Abaixo, clicar em CRIADO POR TRABALHO;
No menu em cima, clique em MÉTRICAS para visualizar as informações;
Feito isso, volta para MODELOS, no menu esquerdo;
Seleciona o modelo;
Clica em PONTOS DE EXTREMIDADE, no menu acima;
TESTAR;
Vai aparecer códigos;
Clicar em TESTAR novamente e vai aparecer um outro código à direita;
Esse código é o resultado procurado.
