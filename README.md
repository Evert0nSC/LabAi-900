# LabAi-900
 Laboratório do Azure IA-900
 
Passo a passo

No estúdio Azure Machine Learning, veja a página Automated ML (em Criação).

Crie um novo trabalho de ML automatizado com as seguintes configurações, usando Next conforme necessário para avançar pela interface do usuário:

Configurações básicas:

Nome do trabalho: mslearn-bike-automl

Novo nome do experimento: mslearn-bike-rental

Descrição: Aprendizado de máquina automatizado para previsão de aluguel de bicicletas

Etiquetas: nenhum

Tipo de tarefa e dados:

Selecione o tipo de tarefa: Regressão

Selecionar conjunto de dados: Crie um novo conjunto de dados com as seguintes configurações:

Tipo de dados:

Nome: aluguel de bicicletas

Descrição: dados históricos de aluguel de bicicletas

Tipo: Tabular

Fonte de dados:

Selecione Dos arquivos da web

URL da Web:

URL da web: https://aka.ms/bike-

aluguéis

Ignorar validação de dados: não selecionar

Configurações:

Formato de arquivo: Delimitado

Delimitador: Vírgula

Codificação: UTF-8

Cabeçalhos de coluna: apenas o primeiro arquivo possui cabeçalhos

Pular linhas: nenhuma

O conjunto de dados contém dados multilinhas: não selecione

Esquema:

Incluir todas as colunas exceto Caminho

Revise os tipos detectados automaticamente

Selecione Criar. Depois que o conjunto de dados for criado,

selecione o conjunto de dados de aluguel de bicicletas para continuar enviando o trabalho de ML #automatizado.

Configurações de tarefa:

Tipo de tarefa: Regressão

Conjunto de dados: aluguel de bicicletas

Coluna de destino: Aluguéis (inteiro)

Configurações adicionais:

Métrica primária: erro quadrático médio normalizado

Explique o melhor modelo: Não selecionado

Usar todos os modelos suportados: desmarcado.

Você restringirá o trabalho para tentar apenas alguns algoritmos específicos

Modelos permitidos: Selecione apenas RandomForest e LightGBM — normalmente você gostaria de tentar o #máximo possível, mas cada modelo adicionado aumenta o tempo necessário para executar o trabalho.
Limites: expanda esta seção

Máximo de testes: 3

#Máximo de testes simultâneos: 3

#Máximo de nós: 3

Limite de pontuação da métrica: 0085 (de modo que, se um modelo atingir uma pontuação métrica de erro quadrático médio normalizado de 0,085 ou menos, o trabalho será encerrado.)

Tempo limite: 15

Tempo limite de iteração: 15

Habilitar rescisão antecipada: selecionado

Validação e teste:

Tipo de validação: divisão de validação de trem

Porcentagem de dados de validação: 10

Conjunto de dados de teste: Nenhum

Calcular:

Selecione o tipo de computação: sem servidor

Tipo de máquina virtual: CPU

Camada de máquina virtual: Dedicada

Tamanho da máquina virtual: Standard_DS3_V2*

Número de instâncias: 1

* Se a sua assinatura restringir os tamanhos de VM disponíveis para você, escolha qualquer tamanho disponível

Envie o trabalho de treinamento. Ele inicia automaticamente

Espere o trabalho terminar

Pode demorar um pouco – agora pode ser um bom momento para uma pausa para o cafe
