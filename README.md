# Robô para testes automatizados de validação de login em aplicações Web

#### Aluno: [Márcio Magalhães](https://github.com/marciolucm)
#### Orientador: [Felipe Borges](https://github.com/FelipeBorgesC)

---

Trabalho apresentado ao curso [BI MASTER](https://ica.puc-rio.ai/bi-master) como pré-requisito para conclusão de curso e obtenção de crédito na disciplina "Projetos de Sistemas Inteligentes de Apoio à Decisão".

<!-- para os links a seguir, caso os arquivos estejam no mesmo repositório que este README, não há necessidade de incluir o link completo: basta incluir o nome do arquivo, com extensão, que o GitHub completa o link corretamente -->
- [Link para o código](https://github.com/link_do_repositorio). <!-- caso não aplicável, remover esta linha -->


---

### Resumo

<!-- trocar o texto abaixo pelo resumo do trabalho, em português -->

Muitos serviços estão sendo disponibilizados na internet e precisamos ter meios para verificar se eles estão disponíveis para os usuários por meio de testes automatizados. Neste trabalho, desenvolvo um robô para efetuar o login num serviço de hospedagem na internet, verificando a disponibilidade e o desempenho da aplicação, coletando dados como os tempos de login e a mensagem obtida, gerando um gráfico com os tempos obtidos e o resultado do desempenho médio do tempo de login.

### 1. Introdução

	Com a pandemia ocorrida em 2020, muitas empresas e órgãos governamentais tiveram que disponibilizar seus serviços de forma digital através da internet, já que o acesso físico e o modelo de atendimento tradicional eram complicados devido a transmissão do vírus.
	Com muitos serviços sendo disponibilizados pela internet, uma forma que está sendo usada para verificar a disponibilidade e desempenho é a utilização de testes automatizados com o uso de robôs. Existem ferramentas que fazem estes testes como JMeter e o Dynatrace. A grande vantagem de utilizar um robô para teste automatizado é que ele simula um acesso de usuário, antecipando possíveis problemas com o serviço e podendo alertar a equipe que suporta a aplicação, de modo a manter a aplicação disponível 24 x 7.


### 2. Modelagem

	Neste trabalho, utilizando Python com Selenium, desenvolvo uma pequena aplicação automatizada para validar o login num serviço de hospedagem, verificando a disponibilidade e o desempenho do serviço. O teste é realizado no site do Booking (https://www.booking.com), que é considerado o maior site de reservas de hotéis do mundo, com mais de 20 anos de atuação, líder de mercado.
	No desenvolvimento do trabalho, foram utilizados as bibliotecas e funções do Selenium para criar um webdriver virtual (Chrome) utilizando o Google Colab para execução do código em Python. Criei algumas funções e procedimentos para organizar a execução do código como: conversão do tempo devido a diferença de fuso horário, já que o teste é realizado num browser virtual executado na nuvem; diferença de tempo; teste de url; criação do web browser e login na url. 
	Uma das dificuldades do teste é a identificação pelo site que o login está sendo realizado possivelmente por um robô, então tive que fazer um tratamento para simular uma ação pelo usuário de “Press and hold”, pressionar e segurar o ponteiro do mouse em um botão do site. Outro complicador é o tempo que se tem de manter pressionado, pois varia conforme cada teste que é realizado.


### 3. Resultados

	Para simulação dos testes, faço 10 tentativas de login a cada 1 minuto, coletando a data e horário do início e conclusão de login, mensagem do teste e calculando o tempo de login (segundos) realizado na aplicação. Para ilustrar os resultados obtidos, exibo os dados obtidos com os tempos de login e a mensagem obtida. Faço um gráfico com os tempos obtidos e o resultado do desempenho médio do login, considerando o login no tempo normal, desprezando os logins quando identificado pela plataforma como um robô.

### 4. Conclusões

	Com a massificação dos serviços na internet, a utilização de um robô é uma excelente funcionalidade para avaliar a disponibilidade e o desempenho das aplicações, antecipando possíveis problemas como o desempenho, ajudando as equipes de desenvolvimento e infraestrutura a identificar onde ocorre um problema. As aplicações na Web estão cada vez mais críticas e a interrupção nos serviços custam muito caro para empresas e muita insatisfação dos clientes.

---

Matrícula: 192.671.073

Pontifícia Universidade Católica do Rio de Janeiro

Curso de Pós Graduação *Business Intelligence Master*
