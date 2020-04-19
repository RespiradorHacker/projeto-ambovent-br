# projeto-ambovent-br
Projeto de ventilador pulmonar baseado no Ambovent desenvolvido em Israel, porém com algumas modificações.

O princípio de funcionamento mecânico do projeto baseia-se no mesmo princípio do Ambovent de Israel. Porém ao invés de motor de vidro, estamos utilizando motor de passo Nema 23 2,8A com o driver TB6600.

A parte de hardware possuirá 2 sensores de pressão do tipo MPX5010dp, um para controlar a pressão do ar, e outro para medir a pressão diferencial em uma placa de orifício e fazer o controle de fluxo isnpiratório e volume Tidal. Porém eles ainda não foram entregues, então estamos tentando adequar um MPX10dp, que já possuimos, ao microcontrolador Arduino pra começar os testes.

A ideia é fazer com o ventilador dê opção ao operador escolher entre os modos de ventilação VCV e PCV.

Segue abaixo mais detalhes sobre o que pretendemos desenvolver:

Objetivo Geral: Projetar e construir um ventilador pulmonar artificial seguro, de fácil operação e de baixo custo;

Objetivos específicos:

•	Projetar e construir um ventilador pulmonar artificial que possa operar nos modos de ventilação PCV e VCV; 
•	Fornecer parâmetros ventilatórios com valores suficientes para tratar, de forma segura e eficiente, pacientes com Covid-19;
•	Atender os requisitos mínimos de segurança exigidos pela ANVISA e normas ISO ABNT específicas para equipamentos eletromédicos;
•	Estimular participantes do projeto a desenvolver pesquisas e novas soluções voltadas para área da saúde.


d) Justificativa 

Na fase crítica do Covid-19 o paciente que o contém sofre de SDRA (Síndrome de desconforto respiratório agudo), demandando o uso contínuo e prolongado de um respirador pulmonar artificial. Devido ao alto poder de transmissão da doença, a necessidade de utilização de respiradores pulmonares aumentou significativamente, nas últimas semanas, no Brasil e no mundo. É de conhecimento de todos que o Brasil não possui respiradores pulmonares suficiente para atender todos pacientes num possível colapso do sistema de saúde. A manutenção de respiradores defeituosos e a aquisição de novos respiradores nacionais e internacionais não será suficiente pra suprir a demanda. É importante ressaltar também que a maioria dos respiradores já existentes no mercado possuem um preço muito elevado além de várias funções e modos ventilatórios que não atendem especificamente pacientes com Covid 19. 
Assim sendo, é de extrema necessidade que haja alternativas mais simples, baratas e seguras que tenham como objetivo atender especificamente pacientes com Covid-19 e que poderão também atender pacientes portadores de doenças com sintomas semelhantes. um paciente com Covid-19 apresenta SDRA, e os modos de ventilações usados para esse caso são: VCV e PCV. Para tanto um respirador mecânico apenas com esses dois modos, consegue atender pacientes com COVID-19 e com doenças semelhantes. Necessitando assim de menos tecnologia e componentes, facilitando o projeto, os testes e a fabricação do mesmo, além de torná-los mais baratos e de fácil operação. 

e) Produto a ser entregue 

Respirador pulmonar de baixo custo baseado na automatização do ressuscitador tipo Ambu. No qual será possível utilizar dois principais modos de ventilação mecânica: modo VCV (Ventilação controlada a volume) e PCV (Ventilação controlada a Pressão), bem como os alarmes e requisitos mínimos necessários exigidos pela ANVISA.

Detalhes do produto:

	É importante ressaltar que os detalhes citados a seguir podem sofrerem alterações, caso seja necessário, ao longo do desenvolvimento do projeto.
Ao iniciar o uso do respirador pulmonar, será possibilitado ao operador escolher o modo PCV ou VCV. A partir do modo escolhido o operador tem ao seu alcance os seguintes parâmetros de entrada:

Parâmetros de entrada no modo VCV: 
•	Volume corrente entre 200 a 800 ml (alterável de 10 em 10 ml);
•	Fluxo inspiratório entre 10 e 60 L/min (alterável de 2 em 2 L/min); 
•	Frequência respiratória entre 8 e 40 rpm (alterável de 2 em 2 rpm);
•	Pausa inspiratória entre 0,25 e 1,5 seg (alterável de 0,25 em 0,25 seg).
•	Pressão expositiva no final da expiração (PEEP) entre 5 e 20 cmH2O (alterável de 5 em 5 cmH2O).

Parâmetros de entrada no modo PCV:
•	Pressão inspiratória entre 10 e 40 cmH2O (alterável de 2 em 2 cmH2O);
•	Frequência respiratória entre 8 e 40 rpm (alterável de 2 em 2 rpm);
•	Tempo de inspiração entre 0,25 e 5 seg (alterável de 0,1 em 0,1 seg);
•	Pausa inspiratória entre 0,25 e 1,5 seg (alterável de 0,25 em 0,25 seg).
•	Pressão expositiva no final da expiração (PEEP) entre 5 e 20 cmH2O (alterável de 5 em 5 cmH2O).

Para que o operador possa controlar de maneira segura os parâmetros de entrada será mostrado ao mesmo, em uma tela, os parâmetros de saída:


Variáveis monitoradas (parâmetros de saída) mostradas nos 2 modos: 
•	Pressão máxima inspiratória em cmH2O (pressão de pico na inspiração);
•	Pressão de platô em cmH2O;
•	Volume minuto em L/min (frequência multiplicada pelo volume Corrente);
•	Tempo de inspiração em segundos;
•	Relação I:E (relação entre tempos de inspiração e expiração);
•	Pressão expositiva no final da expiração (PEEP) em cmH2O.

O sistema possuirá também os seguintes alarmes:

Alarmes:
•	Alarme regulável para pressão inspiratória máxima maior que o valor inserido (recomendável 40 cmH2O);
•	Alarme regula´vel para pressão de platô maior que o valor inserido (recomendável 30 cmH2O);
•	Alarme regulável para volume corrente maior que o valor inserido;
•	Alarme regulável para PEEP medida maior ou menor que a PEEP inserida manualmente pelo operador.
•	Alarme para falta de eletricidade (nesse caso o ventilador continua funcionando normalmente por meio do no-break).

