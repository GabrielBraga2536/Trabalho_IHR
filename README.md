<div align="justify">

# **CareBot:** Melhoria de Projeto e Otimização da Cinemática Aplicada ao Projeto OmniCare

Trabalho de Interação Humano-Robô (IHR) apresentado ao Centro Universitário [FEI](https://portal.fei.edu.br/), como parte dos requisitos necessários para aprovação na disciplina de Interação Humano-Robô (IHR) (CCR230) do curso de Engenharia de Robôs, orientado pelo Prof. Dr. [Fagner de Assis Moura Pimentel](https://github.com/fagnerpimentel).

## Componentes do Grupo

- Luana Nascimento Karpavicius - 11.122.132-1
- Manuella Valles Egrejas - 11.122.138-8
- Gabriel Braga de Souza Otero - 11.122.155-2
- João Pedro Soares Cabral - 11.122.233-7

## Resumo

CareBot é um robô móvel autônomo desenvolvido para navegação em ambientes hospitalares. Derivado do projeto [OmniCare](https://github.com/Thgm01/OmniCare/tree/main), foi realizada uma reformulação para uma nova configuração mecânica com movimentação diferencial, oferecendo maior estabilidade e precisão. Equipado com um potente sensor LiDAR, o robô é capaz de mapear, se localizar e planejar rotas dentro de um ambiente, com potencial de aplicação em tarefas de assistência hospitalar como o transporte de materiais e guias de pacientes. 

## Introdução

A crescente demanda por serviços de saúde, aliada à necessidade de reduzir riscos de contaminação em ambientes hospitalares, impulsiona o desenvolvimento de soluções tecnológicas capazes de contribuir nas rotinas clínicas. Nesse cenário, robôs móveis autônomos mostram-se como ferramentas promissoras para assumir tarefas logísticas repetitivas, como o transporte de medicamentos, materiais e amostras, aliviando os profissionais de saúde para atividades que exigem maior atenção e análise humana.

O CareBot é um robô móvel autônomo desenvolvido para navegação em ambientes hospitalares, capaz de mapear o espaço ao seu redor, localizar-se de forma idependente e planejar rotas seguras até destinos definidos pelo operador. Com sua configuração mecânica diferencial e tamanho compacto, proporcionando maior estabilidade e precisão de movimento em corredores, elevadores e espaços internos.

**Objetivo em uma frase:** atuar como assistente logístico hospitalar, realizando entregas e deslocamente de forma autônoma e segura.

**Experiência desejada:** interação simples, intuitiva e confiável, reduzindo a carga de trabalho da equipe hospitalar e contribuindo para um ambiente mais eficiente e seguro.


## Público-Alvo e Stakeholders

#### Stakeholders

- **Primários** — Equipe de enfermagem e técnicos hospitalares, principais beneficiados pela redução de tarefas logísticas repetitivas.
- **Secundários** — Gestores hospitalares, interessados na redução de custos operacionais e aumento de eficiência; Médicos e profissionais da saúde, beneficiados pela maior disponibilidade da equipe de enfermagem; Pacientes, que teram seus exames ou medicamentos transportados pelo robô.
- **Anti-Usuários** — Financiadores e instituições de fomento, interessados no impacto e viabilidade do projeto; Staff interno do hospital, como faxineiros, manutentores e todos os envolvidos no ambiente de  operação do robô.

#### Personas

- **Persona primária — Amanda, 34 anos:** técnica de enfermagem, trabalha em um hospital de médio porte e passa grande parte do turno transportando materiais entre alas, o que a afasta dos pacientes. Tem pouca familiaridade com tecnologia avançada e precisa de uma solução simples de operar, sem treinamentos longos. Seu principal interesse no CareBot é ganhar tempo para se dedicar ao cuidado direto dos pacientes.
- **Persona secundária — Dr. Roberto, 52 anos:** diretor administrativo do hospital e busca constantemente formas de reduzir custos operacionais e melhorar a eficiência dos processos. Não interage diretamente com o robô, mas é o tomador de decisão sobre sua adoção. Seu interesse está nos indicadores de desempenho, retorno sobre investimento e conformidade com normas sanitárias.

### Mapa de empatia

<p align="center">
  <img src="images/empatia.png" alt="mapa_empatia" width="600">
</p>

#### Persona - Amanda
- **Vê:** Um ambiente hospitalar movimentado, com corredores longos e pacientes que precisam de atenção constante. Vê colegas sobrecarregados realizando tarefas administrativas e logísticas que poderiam ser delegadas.
- **Ouve:** Comentários de colegas sobre o medo de que a tecnologia substitua funções humanas. Orientações da chefia sobre eficiência e produtividade.
- **Diz e faz:** Passa grande parte do turno transportando materiais, medicamentos e amostras entre alas. Comenta com colegas que "falta tempo para cuidar dos pacientes de verdade".
- **Pensa e sente:** Sente-se sobrecarregada e frustrada com tarefas que considera abaixo de sua qualificação. No fundo, deseja ter mais tempo e energia para se dedicar ao que considera o verdadeiro propósito de sua profissão — cuidar de pessoas.
- **Dores:** Tempo excessivo gasto em deslocamentos e tarefas logísticas, cansaço físico ao final do turno por percorrer longas distâncias, sensação de não conseguir atender bem os pacientes por falta de tempo.
- **Ganhos:** Mais tempo disponível para o cuidado direto aos pacientes, redução do cansaço físico no turno de trabalho e maior satisfação profissional ao focar em atividades de maior valor.

#### Persona - Dr. Roberto
- **Vê:** Um hospital com custos operacionais crescentes e equipe constantemente sobrecarregada. Observa profissionais qualificados despendendo tempo em tarefas logísticas que poderiam ser automatizadas.
- **Ouve:** Pressões da diretoria por redução de custos e melhoria nos indicadores de qualidade. Relatos da equipe de enfermagem sobre sobrecarga de trabalho e desgaste físico.
- **Diz e faz:** Participa de reuniões estratégicas buscando soluções para otimizar processos internos. Analisa planilhas de custos operacionais e indicadores de desempenho da equipe.
- **Pensa e sente:** Sente a responsabilidade de modernizar o hospital sem comprometer a segurança dos pacientes e funcionários. Deseja que o hospital seja reconhecido como referência em inovação na área da saúde.
- **Dores:** Dificuldade em justificar o investimento inicial no robô para a diretoria, receio de problemas técnicos que possam interromper o fluxo hospitalar e incerteza sobre o tempo necessário para o retorno do investimento.
- **Ganhos:** Redução de custos operacionais com otimização da logística interna, melhora nos indicadores de satisfação de pacientes e funcionários, e posicionamento do hospital como referência em inovação tecnológica.


## Contexto de uso

O CareBot trabalha dentro de um hospital de médio porte com vários andares. A tarefa liga pontos de origem, como postos de enfermagem e alas de internação, a pontos de destino, como laboratório de análises clínicas, farmácia e CME. Para isso, o robô precisa passar por corredores longos e compartilhados por macas, cadeiras de rodas, carrinhos de medicação e de limpeza, pacientes com mobilidade reduzida; e elevadores que são espaços confinados e divididos com pessoas, a porta tem tempo de abertura limitado, a soleira tem vãos e desníveis.


## Jornada do usuário


**1. Solicitação (início da tarefa)**
- Amanda abre a interface (tela do posto ou tablet), escolhe *"Enviar material"*, define o destino *Laboratório – 1º andar* e a prioridade.

**2. Deslocamento até a usuária**
- O robô anda pelo **lado direito** do corredor, em velocidade reduzida. Ele passa por pessoas mantendo pelo menos a **zona pessoal (≥ 0,5–1,2 m)**. Se encontra pessoas conversando, contorna o grupo e **nunca passa entre elas**. Diante de quem anda devagar, reduz a velocidade e espera uma brecha.

**3. Aproximação e cumprimento**
- O robô chega **pela frente** de Amanda, dentro do campo de visão dela, e não por trás. Para a cerca de **1,2 m**, na fronteira entre a zona pessoal e a zona social de Hall, e vira a frente, onde ficam a tela e as prateleiras, na direção dela.

**4. Carregamento e confirmação**
- Amanda coloca as amostras na prateleira e toca em *"Confirmar envio"*.

**5. Navegação até o elevador**
- Se o caminho estiver totalmente bloqueado, o robô para, espera alguns segundos e diz: *"Com licença, posso passar?"*. Se continuar bloqueado, recalcula a rota.

**6. Uso do elevador (momento mais delicado)**
- **Espera:** o robô se posiciona **ao lado da porta, não na frente dela**, para não atrapalhar quem sai. Chama o elevador pela interface dedicada ou pelo acionamento físico do botão, conforme a solução escolhida.
- **Prioridade:** quando a porta abre, o robô avalia a ocupação com o LiDAR e a câmera. Se houver **maca, cadeira de rodas ou cabine cheia**, ele **cede a vez**: *"Pode ir, eu aguardo o próximo."* O LED fica **âmbar**.
- **Entrada:** com espaço livre, ele diz *"Com licença"* e entra devagar, atravessando a soleira em linha reta. A tração diferencial com rodas convencionais foi escolhida justamente para vencer esse desnível com estabilidade. Ele fica **junto ao fundo ou à lateral da cabine**, ocupando o menor espaço possível e com a frente virada para a porta.
- **Dentro da cabine:** o robô fica **parado e em silêncio**. Não gira nem se movimenta perto dos passageiros. A tela mostra *"Indo para o 1º andar"*, para que as pessoas entendam por que ele está ali.
- **Identificação do andar:** o andar é reconhecido pelo visor (visão computacional) ou pelo sinal da interface. Ao chegar, o robô **troca o mapa** para o do 1º andar.
- **Saída:** espera os passageiros mais próximos da porta saírem primeiro. Depois diz *"Com licença, este é meu andar"* e sai.

**7. Entrega no laboratório**
- O técnico retira as amostras e confirma na tela. O robô responde: *"Entrega concluída. Obrigado!"*

## Análise de concorrência

- **Aethon Zena RX (ST Engineering Aethon, EUA):** Sucessor do TUG T2 para farmácias e laboratórios, tem navegação com desvio de obstáculos e localização 8 vezes mais rápidas, mais de 10.000 polegadas cúbicas de capacidade (2,6 vezes a do T2), interface por toque que exige quase nenhum treinamento e 10 horas de operação contínua. O gabinete tem quatro compartimentos com trava independente, acessados por biometria ou PIN.

<p align="center">
  <img src="images/ZENA_RX.png" alt="ZENA_RX" width="370">
</p>

- **Pudu FlashBot (Pudu Robotics, China):** Pesa 55 kg, carrega 30 kg (15 kg por bandeja) e tem velocidade ajustável entre 0,5 e 1,5 m/s. Mede cerca de 54 × 53 × 105 cm e tem autonomia de 8 a 12 horas, com recarga automática. 

<p align="center">
  <img src="images/Flash_bot.png" alt="Flash Bot" width="300">
</p>

- **Relay (Relay Robotics, antiga Savioke):**, A versão Relay tem um compartimento único e trancável, indicado para entrega de medicamentos e amostras que exigem transporte seguro em hospitais. O software permite rastrear a cadeia de custódia e exigir senha para abrir o compartimento.

<p align="center">
  <img src="images/relay_robot.jpg" alt="Relay_Robot" width="600">
</p>

#### 1. Existe plataforma similiar, que atende o mesmo mercado e funcionalidades?
O Zena RX Foi desenhado especificamente para o hospital, com foco em farmácia e laboratório.

- *Pontos positivos:*
  - A segurança é a mais completa dos robôs analisados. O gabinete é todo de metal, com portas travadas fisicamente, biometria e senhas individuais da equipe. 
  - Faz até 4 entregas seguras por viagem. Isso reduz o número de viagens. 
  - Integra-se com elevadores de todas as marcas e com sistemas de portas         automáticas. 
  - A capacidade é de cerca de 164 L, o que permite levar desde frascos pequenos até caixas grandes na mesma viagem, e há exigência de dupla autenticação na cadeia de custódia. 
  - No laboratório, a proposta é evitar o sistema de tubos pneumáticos. 

- *Pontos negativos:*
  - O site não divulga preço e direciona para agendar uma conversa comercial. 
  - É especializado em farmácia e laboratório. Para transportar carrinhos inteiros, a Aethon oferece outro modelo, o T3. O cliente teria de combinar robôs diferentes. 
  - É um produto fechado e importado. Isso implica custo alto, dependência do fabricante para suporte e pouca possibilidade de adaptação ao contexto brasileiro.

#### 2. Existe plataforma diferente quanto ao serviço, mas que atenda esse mercado?
O FlashBot nasceu como robô de entrega de prédios (hotéis e escritórios), mas também é oferecido para hospitais.

- *Pontos positivos:*
  - É anunciado para transportar medicamentos, refeições, roupa de cama e suprimentos entre andares. 
  - Usa IoT em nuvem para chamar elevadores automaticamente, e vários robôs podem cooperar entre si. 
  - Os compartimentos são ajustáveis (de dois a quatro) e têm acesso seguro. 
  - Tem escala de produção grande: quase 80 mil unidades enviadas para mais de 60 países. 
  - A versão atualizada também opera em áreas semiexternas, como jardins de hospitais. 
  - O custo tende a ser menor: um revendedor lista o robô a US$ 20.000, com a observação de que preços na América Latina podem variar. 

- *Pontos negativos:*
  - É um robô generalista.Não dispôe recursos hospitalares como biometria ou rastreio de cadeia de custódia, que o Zena RX e o Relay oferecem.
  - A carga de 30 kg e os compartimentos de bandeja atendem melhor a suprimentos leves do que a materiais clínicos sensíveis.
  - Não contém informações suficiente sobre conformidade com normas sanitárias, o que seria necessário verificar antes de uma aplicação hospitalar real.


#### 3. Quais plataformas nossa equipe acha mais interessantes?

Pudu FlashBot é a mais interessante como referência de produto para o CareBot. Está na mesma faixa de porte (base de cerca de 54 × 53 cm, próxima aos 52 × 40 cm do CareBot) e de custo, e mostra que dá para atender hospitais com um robô compacto e acessível, sem a complexidade de um robô exclusivamente clínico. Ela também reforça a escolha da tração diferencial e do Nav2 para corredores estreitos.

Aethon Zena RX é a mais interessante como meta de funcionalidade futura. O que ela tem de mais valioso para o CareBot é o acesso autenticado aos compartimentos, que responde à preocupação com segurança e rastreabilidade da persona Dr. Roberto.

Posicionamento do CareBot: o FlashBot é generalista e acessível, e o Zena RX é especializado e premium. Fica um espaço para um robô aberto (ROS2 + Nav2), de baixo custo, com recursos mínimos de segurança hospitalar, voltado a hospitais que não têm orçamento para plataformas como o Zena RX.

## Design do Robô

#### Forma, função e affordances

- **Acessibilidade física**

  - *Altura de carga:* com cerca de 57 cm, o robô obriga uma pessoa em pé a se abaixar para colocar ou retirar itens. Isso vai contra o que a persona Ana busca (menos cansaço físico). A chapa superior mais alta, ou uma bandeja elevada, resolveria. Uma pessoa em cadeira de rodas, por outro lado, alcança bem esse nível.
  - *Altura de detecção:* o LiDAR fica a cerca de 22 cm do chão. Ele vê pernas e paredes, mas não vê obstáculos suspensos (mesas, macas, suportes de soro). Isso é uma limitação de segurança para pessoas com mobilidade reduzida.
  - *Porte:* a base de 52 × 40 cm cabe bem em corredores e deixa espaço para passagem de macas e cadeiras de rodas.
  - *Higienização:* perfis estruturais de alumínio costumam ter ranhuras, e chapas abertas acumulam sujeira. Em hospital, isso dificulta a limpeza.
<br>

- **Acessibilidade sensorial e cognitiva**

  - Pessoas com deficiência visual ou auditiva precisam de sinais redundantes de presença e intenção, como luz e som juntos.
  - Hoje o operador dá o destino pelo RViz, que é uma ferramenta técnica. Para a Ana, o ideal é uma interface com poucos botões ou toque, quase sem treinamento.
  - O robô só opera em um andar. Elevadores e portas ainda não estão integrados, o que limita a autonomia real em hospitais com vários andares.

#### Grau de antropomorfismo

##### 1. Posição no espectro máquina ↔ humano

```
Máquina ●────────────────────────────── Humano
        1  2  3  4  5  6  7  8  9  10
```
Hoje, o CareBot fica em 1 de 10, no padrão “robject” (objeto funcional que se move) com tendência minimalista.

- Nada na forma lembra um corpo. Não há cabeça, olhos, rosto ou braços. A geometria é de prateleiras sobre rodas.
- A forma segue a função. Cada elemento tem um propósito técnico (chapas para carga, rodas para locomoção, LiDAR para percepção). Nenhum existe para parecer humano ou animal.
- Não é zoomórfico. Também não evoca um animal de estimação.
- O comportamento é a única fonte de “vida”. O robô se move sozinho, escolhe caminhos e para diante de obstáculos. Isso faz as pessoas atribuírem intenções a ele, mesmo sem rosto, como acontece com aspiradores robô. Esse efeito vem do movimento, e não do design.
<br>

##### 2. Qual padrão é mais aceito pela sociedade no contexto desse projeto?

O padrão mais aceito é o de máquina ou minimalista, complementado por poucos sinais sociais abstratos. Essa conclusão vem do próprio mercado: os robôs de logística hospitalar analisados têm formato de gabinete ou carrinho, sem traços humanos. O Zena RX, por exemplo, é essencialmente um gabinete com compartimentos trancáveis.

Há também uma questão de expectativas. Um robô com aparência humana sugere que ele conversa, compreende e participa do cuidado direto, mas o CareBot apenas transporta itens entre pontos definidos. Manter um design de máquina evita a frustração de uma promessa que o robô não cumpre, em linha com a ideia de prometer menos e entregar mais. O ambiente hospitalar reforça essa escolha, já que pacientes fragilizados e crianças tendem a reagir pior a algo ambíguo ou “quase humano” do que a algo claramente identificável como máquina.
<br>

##### 3. Como evitar o vale da estranheza

O vale da estranheza, conceito proposto por Masahiro Mori em 1970, descreve o desconforto causado por robôs que são quase humanos, mas apresentam falhas sutis que os tornam inquietantes. Como o CareBot está em 1 numa escala de 10 de antropomorfismo, o risco hoje é muito baixo. A estratégia do grupo, portanto, é não entrar nessa região, mantendo coerência entre aparência e comportamento.
<br>

### Padrões de design

> 💡
> Identifique **2 padrões de design** (design patterns) aplicáveis ao seu projeto e explique como eles se **combinam**.

<details>
<summary>📄</summary>

**"Apresentação inicial"** (o robô se apresenta brevemente antes de perguntar o destino) + **"em movimento junto"** (anda ao lado/à frente do grupo, ajustando o ritmo ao visitante mais lento) — combinados, formam o padrão composto de "robô guia turístico".

</details>

### Valores e ética

Dois valores importantes para o CareBot são segurança e privacidade. A segurança deve orientar o planejamento das rotas e o comportamento do robô diante de obstáculos e pessoas. Já a privacidade deve ser preservada, evitando a coleta ou o armazenamento desnecessário de informações pessoais dos pacientes e profissionais.

Um risco ético é que o robô provoque acidentes ou bloqueie a passagem em áreas de grande circulação, principalmente quando houver pacientes com mobilidade reduzida. Para reduzir esse risco, o CareBot deve operar com velocidade controlada, manter distância adequada das pessoas e priorizar a parada quando não houver condições seguras para continuar.

### Protótipo no papel

<p align="center">
  <img src="images/prototipo_papel.png" alt="Relay_Robot" width="600">
</p>

(Corpo afunilado sobre uma base omnidirecional (três rodas onidirecionais, em arranjo triangular); "cabeça" arredondada com dois olhos, uma antena/sensor no topo; tela na parte de cima do torso, com o nome do robô; sem braços — apenas um anel de luz na base para sinalizar status. Altura total ≈1,55 m; diâmetro da base ≈0,90 m.)

## Ações do robô

Para cumprir sua rotina de entregas entre os andares do hospital, o CareBot realiza quatro ações principais de forma coordenada:


#### 1. Deslocamento pelos corredores (Navegação horizontal)

- **Descrição da ação:** 
  - O CareBot se desloca de forma autônoma pelos corredores hospitalares utilizando o sistema de navegação Nav2 no ROS 2 Jazzy Jalisco
  - A locomoção é feita por duas rodas motorizadas na parte de trás e duas rodas de apoio na frente, garantindo um andar mais firme e sem os escorregões que aconteciam antes
  - O robô anda sempre pelo lado direito do corredor e em velocidade moderada, aproveitando seu tamanho compacto para não atrapalhar a passagem
  - Respeita o espaço pessoal das pessoas (mantendo entre 0,5 m e 1,2 m de distância), desacelera quando encontra alguém caminhando devagar e contorna colegas conversando sem passar no meio deles.
  - Usa seu sensor LiDAR para enxergar o caminho, reconhecer onde está e desviar de pessoas e carrinhos em tempo real

- **Pré-requisitos:** 
  - Destino e prioridade definidos pela enfermagem na tela do posto ou no tablet.
  - Mapa do andar carregado no sistema do robô
  - Robô ciente de sua localização exata no corredor.
  - Bateria com carga suficiente para fazer a entrega e retornar.
  - Materiais colocados nas prateleiras e envio confirmado pelo profissional.
  - Nenhuma trava ou botão de segurança acionado.

- **Modificações esperadas no ambiente:** 
  - Deslocamento físico do robô e dos materiais até a área de entrega.
  - Posto de origem desocupado, permitindo o fluxo livre da equipe.
  - Convivência harmoniosa nos corredores, com pedestres notando sua presença sem sustos.
  - Atualização do status da tarefa para a equipe acompanhar o trajeto.


#### 2. Uso do elevador entre os andares (Navegação vertical)

- **Descrição da ação:** 
  - Ao chegar ao saguão, o robô espera ao lado da porta do elevador (nunca bem na frente) para não impedir a saída de quem está lá dentro.
  - Chama o elevador de forma automática pelo sistema do hospital ou por acionamento planejado.
  - Quando a porta abre, o robô verifica o espaço interno; se avistar macas, cadeiras de rodas ou a cabine cheia, ele cede a vez com gentileza, acende suas luzes em tom âmbar e fala: *"Pode ir, eu aguardo o próximo."*
  - Com espaço livre, pede licença (*"Com licença"*) e entra em linha reta.
  - O novo par de rodas traseiras ajuda a vencer o pequeno desnível e o vão do elevador com firmeza e suavidade.
  - Dentro da cabine, posiciona-se no fundo ou na lateral, virado de frente para a porta, em silêncio e com a tela informando o andar para onde está indo.
  - Ao chegar ao andar certo, espera as pessoas saírem primeiro, avisa (*"Com licença, este é meu andar"*) e sai com cuidado.

- **Pré-requisitos:** 
  - Rota que exija troca de andar para completar a entregas.
  - Porta do elevador completamente aberta.
  - Espaço interno suficiente e sem passageiros prioritários (macas ou cadeirantes).
  - Robô alinhado de frente para a soleira para passar sem prender as rodas.
  - Reconhecimento do elevador e do andar ativo via câmera ou comunicação integrada.

- **Modificações esperadas no ambiente:** 
  - Robô e materiais transportados de forma segura até o outro andar.
  - Carregamento automático do mapa do novo pavimento no sistema de navegação.
  - Espaço do elevador compartilhado com tranquilidade, sem assustar os passageiros.
  - Cabine livre e desocupada assim que a descida/subida é concluída.


#### 3. Entrega de materiais no destino (Interação de entrega)

- **Descrição da ação:** 
  - O robô chega à sala de destino (como laboratório ou farmácia) e vai desacelerando aos poucos.
  - Faz uma aproximação pela frente do profissional de saúde, parando a uma distância confortável de conversa ($\approx 1{,}2\text{ m}$).
  - Gira o corpo para posicionar as prateleiras e a tela de toque de frente para a pessoa, facilitando o alcance.
  - Mostra na tela o resumo da entrega e pede que retirem os itens com calma.
  - Assim que a retirada é confirmada com um toque na tela, agradece cordialmente: *"Entrega concluída. Obrigado!"*.
  - Fica pronto para voltar à sua base ou seguir para uma próxima chamada.

- **Pré-requisitos:** 
  - Chegada ao ponto correto de entrega sem desvios de posição.
  - Presença de um funcionário autorizado no local para receber os itens.
  - Motores completamente parados e travados para dar firmeza enquanto a pessoa mexe nas prateleiras.
  - Espaço livre em volta do robô para facilitar o acesso do profissional.

- **Modificações esperadas no ambiente:** 
  - Retirada das amostras ou remédios das prateleiras do robô para as mãos da equipe.
  - Entrega marcada como finalizada no sistema do hospital.
  - Robô pronto para descansar na base ou atender ao próximo chamado da enfermagem.
  - Espaço de trabalho do laboratório ou farmácia liberado logo após a entrega.


#### 4. Parada de segurança e pedido de passagem

- **Descrição da ação:** 
  - Ao notar uma parada repentina de alguém à frente, a chegada de uma maca de emergência ou o corredor bloqueado por carrinhos, o robô para suavemente na mesma hora.
  - Aguarda alguns instantes em silêncio para ver se a pessoa ou obstáculo vai se mover.
  - Acende luzes de alerta para sinalizar que está aguardando vez.
  - Se continuar bloqueado, pede licença com voz calma e amigável: *"Com licença, posso passar?"*.
  - Se o bloqueio continuar após o aviso, busca sozinho um caminho alternativo para contornar a área.

- **Pré-requisitos:** 
  - Sensor LiDAR detectando algo ou alguém muito próximo da frente do robô (menos de 0,5 m).
  - Caminho habitual temporariamente bloqueado.
  - Identificação de obstáculos no piso que possam atrapalhar a passagem segura das rodas.

- **Modificações esperadas no ambiente:** 
  - Segurança total para pedestres e pacientes, prevenindo qualquer esbarrão ou susto.
  - Reação natural e compreensiva das pessoas ao redor, liberando passagem de forma voluntária ao ouvir o robô pedir licença.
  - Caminho recalculado pelo robô para contornar o obstáculo sem travar o trânsito do hospital.
  - Proteção e cuidado com a integridade dos remédios e frascos transportados.

## Interações do robô

A comunicação do CareBot com as pessoas acontece por três canais complementares: o espacial, o verbal e o não-verbal. Como discutido anteriormente, o robô ocupa a posição 1 na escala de antropomorfismo e não possui cabeça, olhos ou braços; por isso, sua comunicação depende, principalmente, da forma como se movimenta, da tela, das luzes de LED e de um conjunto restrito de falas. Os três canais foram pensados para funcionar juntos, já que um sinal isolado pode ser ignorado em um corredor hospitalar movimentado.

### Espacial

Para definir a posição do robô em relação ao usuário, utiliza-se como base o modelo de proxêmica de Hall, que divide o espaço ao redor de uma pessoa em zonas íntima, pessoal, social e pública. Durante o deslocamento, o CareBot mantém-se, no mínimo, na zona pessoal (entre 0,5 m e 1,2 m) ao passar por alguém. Já nas interações de coleta e entrega, para a cerca de 1,2 m, na fronteira entre a zona pessoal e a zona social, distância que permite à pessoa alcançar as prateleiras e a tela sem que o robô invada seu espaço.

Além disso, utiliza-se o conceito de F-formation para orientar o corpo do robô. Na coleta e na entrega, robô e profissional formam uma configuração face a face (*vis-à-vis*), com a frente do robô, onde ficam a tela e as prateleiras, voltada para a pessoa. Dessa forma, o espaço compartilhado entre os dois (*o-space*) coincide, nesse caso, com a própria área de carga. Quando encontra pessoas conversando, o robô reconhece o *o-space* formado pelo grupo e o trata como uma área a ser contornada, e nunca atravessada.

A interação é sempre iniciada pela frente, dentro do campo de visão da pessoa, e nunca por trás, já que uma aproximação inesperada causa susto e desconfiança. O robô reduz a velocidade gradualmente à medida que se aproxima e, antes de partir, gira a frente na direção em que vai seguir, enquanto a tela exibe o destino. Assim, quem está por perto consegue antecipar a trajetória do robô antes mesmo de ele se mover.

#### 1. Aproximação para coleta e entrega

- **Descrição:** o robô chega pela frente do profissional, desacelera aos poucos, para a cerca de 1,2 m e gira o corpo para que a tela e as prateleiras fiquem voltadas para a pessoa.
- **Pré-requisitos:**
  - Profissional localizado pelo LiDAR e pela câmera no ponto de origem ou de destino.
  - Espaço livre à frente da pessoa para que o robô se posicione sem bloquear a passagem.
  - Tarefa de coleta ou de entrega ativa no sistema.
- **Resposta emocional esperada:** tranquilidade e sensação de controle, uma vez que a pessoa vê o robô chegando, sabe o que ele espera dela e não precisa se deslocar para alcançá-lo.

#### 2. Passagem por pessoas no corredor

- **Descrição:** o robô anda pelo lado direito do corredor, em velocidade reduzida, mantendo a zona pessoal das pessoas que cruza. Diante de alguém parado, desvia mantendo essa distância; diante de quem anda devagar, reduz a velocidade e aguarda uma brecha para ultrapassar; diante de pessoas conversando, contorna o grupo por fora, sem passar entre elas. Para grupos maiores, que ocupam toda a largura do corredor, o robô para e aguarda uma abertura natural na formação.
- **Pré-requisitos:**
  - Mapa do andar carregado e localização do robô estabelecida.
  - Pessoas detectadas pelo LiDAR, com estimativa de posição e direção de deslocamento.
  - Largura de corredor suficiente para o desvio; caso contrário, aplica-se a parada de segurança descrita nas ações do robô.
- **Resposta emocional esperada:** indiferença confortável, isto é, as pessoas percebem o robô, mas não precisam interromper o que fazem nem mudar seu trajeto por causa dele.

#### 3. Posicionamento no elevador

- **Descrição:** o robô espera ao lado da porta, e não na frente dela, liberando a saída de quem está na cabine. Ao entrar, ocupa o fundo ou a lateral, com a frente voltada para a porta, e permanece parado até chegar ao andar de destino.
- **Pré-requisitos:**
  - Rota que exija troca de andar.
  - Porta totalmente aberta e espaço interno livre, sem macas ou cadeiras de rodas.
- **Resposta emocional esperada:** segurança e previsibilidade, já que, em um espaço confinado, o robô ocupa pouco espaço e não se movimenta perto dos passageiros.

#### Ajuste para outro contexto de uso

O comportamento descrito acima considera corredores de alas de internação. Em um pronto-socorro, entretanto, o fluxo de macas de emergência é intenso e imprevisível, fazendo com que um desvio lento se torne um obstáculo para o atendimento. Por isso, nesse contexto, o robô deve aumentar a distância mantida em relação a macas e equipes em deslocamento, preferir trajetos junto à parede e, ao detectar uma maca se aproximando, encostar-se lateralmente e parar até que ela passe, em vez de tentar contorná-la.


### Verbal

A interação verbal do CareBot é restrita a um conjunto fechado de falas associadas a cada situação. Essa escolha se justifica por três motivos. Primeiramente, as falas necessárias são poucas e previsíveis (pedir passagem, ceder a vez), o que não exige uma conversa aberta. Em seguida, como estabelecido na seção de valores e ética, a privacidade deve ser preservada, e um modelo de linguagem aberto tenderia a coletar e processar falas de pacientes e profissionais sem necessidade. Por fim, um robô que conversa livremente sugere capacidades sociais que o CareBot não possui, contrariando a ideia de prometer menos e entregar mais adotada no design.

#### 1. Pedido de passagem

- **Descrição:** ao encontrar o caminho bloqueado, o robô para, aguarda alguns segundos em silêncio e, se o bloqueio continuar, diz: *"Com licença, posso passar?"*. Se ainda assim não houver passagem, recalcula a rota sem insistir no pedido.
- **Pré-requisitos:**
  - Obstáculo ou pessoa detectado a menos de 0,5 m da frente do robô.
  - Tempo de espera inicial esgotado sem que o caminho tenha sido liberado.
- **Resposta emocional esperada:** cordialidade e disposição em colaborar, já que o pedido é educado, curto e só acontece depois de o robô ter esperado.

#### 2. Comunicação no elevador

- **Descrição:** ao ceder a vez, o robô diz *"Pode ir, eu aguardo o próximo."*; ao entrar, *"Com licença"*; e, ao sair, *"Com licença, este é meu andar"*. Dentro da cabine, permanece em silêncio, enquanto a tela informa o andar de destino.
- **Pré-requisitos:**
  - Elevador com a porta aberta e ocupação avaliada pelo LiDAR e pela câmera.
  - Andar de destino reconhecido pelo visor ou pela interface integrada.
- **Resposta emocional esperada:** compreensão e conforto, uma vez que os passageiros entendem por que o robô está ali e o que ele vai fazer, sem se sentirem pressionados a dar espaço.

#### Timing

O robô não usa marcadores conversacionais vocais, como "uh-huh", já que eles sugeririam uma capacidade de diálogo que ele não possui. Em seu lugar, ao receber um toque na tela, emite um sinal sonoro curto e altera a cor do LED, confirmando, imediatamente, que a ação foi registrada e evitando um silêncio ambíguo. Além disso, o robô não fala enquanto detecta alguém falando por perto, aguardando uma pausa antes de pedir licença, e nunca repete o mesmo pedido em sequência, o que soaria insistente.

### Não-verbal

Como dito anteriormente, o CareBot não possui rosto nem braços, o que descarta canais como o olhar e o gesto. Por isso, os dois canais não verbais escolhidos são a **postura**, entendida aqui como a orientação do corpo do robô, e o **ritmo**, isto é, a velocidade e a suavidade de seus movimentos.

#### 1. Orientação do corpo (postura)

- **Descrição:** a frente do robô, onde ficam a tela e as prateleiras, funciona como sua "face". Ao chegar a um profissional, o robô gira essa frente na direção da pessoa, sinalizando que a interação começou; ao terminar, gira na direção da próxima rota, sinalizando que vai partir. No elevador, a frente voltada para a porta indica que o robô aguarda o seu andar.
- **Pré-requisitos:**
  - Posição da pessoa ou da porta identificada pelo LiDAR e pela câmera.
  - Espaço livre ao redor do robô para que ele gire sem encostar em ninguém.
- **Resposta emocional esperada:** clareza e atenção, já que a pessoa entende, sem precisar de uma fala, quando o robô está disponível para ela e quando está de saída.

#### 2. Velocidade e suavidade do movimento (ritmo)

- **Descrição:** o robô desacelera de forma gradual ao se aproximar de alguém, acompanha o passo de quem anda devagar à sua frente e para de maneira suave, sem frenagens bruscas. Um movimento lento e contínuo comunica cuidado; uma parada completa comunica que o robô está cedendo passagem.
- **Pré-requisitos:**
  - Pessoas detectadas pelo LiDAR, com estimativa de distância e de velocidade de deslocamento.
  - Controle de velocidade com rampas de aceleração e desaceleração configuradas no Nav2.
- **Resposta emocional esperada:** confiança e ausência de susto, uma vez que o comportamento do robô é previsível e coerente com o de alguém que respeita o espaço dos outros.


## Emoção

A expressão de emoções em um robô de logística hospitalar exige cuidado. Como discutido anteriormente, o CareBot não participa do cuidado direto dos pacientes e deve manter coerência entre aparência e comportamento; entretanto, ele circula diariamente entre pessoas que podem estar cansadas, apressadas, preocupadas ou fragilizadas. Por isso, o objetivo não é que o robô "sinta" ou demonstre emoções intensas, mas que reconheça, de forma simples, o estado de quem está por perto e ajuste seu comportamento para não agravar uma situação já delicada.

### Percepção do estado emocional do usuário

Utilizando-se dos sensores que o robô já possui, é possível estimar, principalmente, a dimensão de ativação a partir de pistas comportamentais simples:

- **Movimento (LiDAR):** a velocidade e a direção de deslocamento de uma pessoa indicam pressa ou urgência, como no caso de uma equipe que corre em direção a um quarto ou de alguém que conduz uma maca rapidamente.
- **Voz (microfone):** o volume e a intensidade da fala, e não o seu conteúdo, indicam um ambiente tenso ou uma pessoa alterada, sem que seja necessário gravar ou transcrever o que foi dito.
- **Interação com a tela:** toques repetidos, cancelamentos seguidos ou longos períodos sem resposta sugerem, respectivamente, impaciência ou dúvida diante da interface.
- **Postura e orientação (câmera):** a câmera permite identificar se a pessoa está voltada para o robô ou de costas e ocupada, sem a necessidade de classificar expressões faciais.

Em coerência com o valor de privacidade estabelecido anteriormente, essas pistas devem ser processadas localmente e descartadas logo após o uso, sem armazenamento de imagens ou de áudio.

### Expressão do robô

Tomando como base o projeto OmniCare, do qual o CareBot deriva, a expressão do robô é construída sobre três recursos. Primeiramente, a sinalização luminosa por LEDs endereçáveis, com transições suaves de cor e brilho, cuja intensidade é ajustada para garantir visibilidade sem causar desconforto a pessoas com hipersensibilidade sensorial. Em seguida, um sinal sonoro curto, que funciona como redundância para pessoas com deficiência visual. Por fim, a tela frontal, que, no OmniCare, exibe uma face simples projetada para transmitir neutralidade, serenidade e segurança, reduzindo a apreensão diante de um robô móvel.

### Gerenciamento de expectativas

Um risco importante surge justamente da tela com face e das respostas cordiais. Se o robô parece reagir ao estado emocional das pessoas, pacientes e acompanhantes podem passar a esperar que ele também compreenda suas necessidades, responda a perguntas sobre exames ou medicamentos, reconheça quem são ou ofereça algum tipo de conforto. O CareBot não consegue cumprir essas expectativas, uma vez que sua interação verbal é restrita e sua função se limita ao transporte de materiais.

Vale notar que, no próprio OmniCare, a face exibida na tela foi tratada como um elemento estético e acolhedor, e não como uma interface de interação, já que não envolve troca de informações nem reconhecimento do usuário. Para o CareBot, adota-se a mesma postura: a face deve permanecer neutra e minimalista, mantendo o robô longe do vale da estranheza, e, quando alguém fizer um pedido fora do seu escopo, a tela deve informar, de forma simpática e direta, que o robô não pode ajudar com aquele assunto e que a pessoa deve procurar a equipe de enfermagem. Dessa forma, o robô é percebido como uma máquina educada e confiável, e não como um assistente capaz de oferecer cuidado.

---                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     
[^1]: Fonte: Adaptado de <https://hazeshift.com.br/mapa-de-empatia/>

</div>