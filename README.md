![banner](./assets/banner.png)

# Oceanet · Edge Computing & Computer Systems

| Integrante | RM |
|---|---|
| [Guilherme Santos Nunes](https://github.com/sannunez) | RM558989 |
| [Henry Evideira Paulo](https://github.com/Hep4xl0) | — |
| [Kaique Zaffarani](https://github.com/Z4ffarani) | RM556677 |

Global Solution 2024.1 · Blue Future · Engenharia de Software · FIAP

---

## O projeto Oceanet

A **[O20](https://www.g20.org/pt-br/g20-social/grupos-de-engajamento/oceans-20)**, em parceria com o projeto Blue Future da **[FIAP](https://www.fiap.com.br)**, está procurando capturar e visualizar dados com métodos de fácil entendimento sobre a saúde dos oceanos e a poluição que os afetam. Com isso, decidimos elaborar um protótipo (e seu simulador) capaz de detectar gases tóxicos no ar, além de medir a temperatura da superfície dos oceanos.

Para o protótipo, consideramos o dióxido de carbono (CO2) como gás a ser detectado, pois ele é, de acordo com pesquisas, um dos principais causadores de acidificação, alteração química e diminuição do pH dos oceanos.

![simulador](assets/img%20-%20simulador.png)

### Projeto principal

[Oceanet](https://github.com/Z4ffarani/Oceanet): repositório principal do projeto.

## Esta entrega: Edge Computing & Computer Systems

| Entregável | Onde |
|---|---|
| Simulador (Tinkercad) | [tinkercad.com/things/caiS2UM6vG7](https://www.tinkercad.com/things/caiS2UM6vG7-gs-simulador?sharecode=H-b8QUJkQ7_S-XZZ2pjAcXow0_1kT6jryNqjPAjow3I) |
| Vídeo explicativo | [youtu.be/aBZ_rd_zkUo](https://youtu.be/aBZ_rd_zkUo) |
| Código do protótipo | [`src/`](src) |
| Bibliotecas dos sensores | [`libraries/`](libraries) |

### Como usar o simulador

Para melhor experiência no simulador, é necessário compreender algumas informações presentes nele:

- **Temperatura:**

  ![medindo temperatura](assets/img%20-%20medindo%20temperatura.png)

  *Para alterar valores de temperatura, basta iniciar a simulação e ajustar o nível clicando no sensor TMP36.*

- **Detecção de gás:**

  ![gás detectado](assets/img%20-%20gas%20detectado.png)

  *Dependendo da distância entre o gás e o sensor MQ-135, é possível visualizar mensagens de alerta. Caso o gás esteja bem próximo do MQ-135 (como na imagem), a sirene é acionada.*

- **Valores:**

  ![alterando valores](assets/img%20-%20alterando%20valores.png)

  *É possível alterar os valores sublinhados de azul, mudando o raio de distância em que cada alerta é transmitido no LCD, apesar de estarem previamente calibrados.*

### Como usar o protótipo

Para total utilização e aperfeiçoamento do sistema de acordo com suas necessidades, é necessário compreender algumas informações essenciais da codificação do protótipo:

- **Fundamentais:**

  ![bibliotecas e definições](assets/img%20-%20bibliotecas%20e%20definições%20com%20entradas%20específicas.png)

  *Esta área já inclui as bibliotecas, define as portas de entrada (números na imagem) e faz a declaração dos sensores no Arduino.*

- **Nível de ppm para o sensor de gás:**

  ![nível de ppm médio](assets/img%20-%20nível%20de%20ppm%20médio.png)

  *Nesta função, a unidade de medida ppm (também nomeada para ser um ponto flutuante), comumente utilizada para registrar a quantidade de gases presente no ambiente (quanto maior o ppm, mais gás está presente), é colocada em uma média entre 350 e 30.000 para o sensor MQ-135 (destinado a detectar dióxido de carbono). A média de ppm pode ser alterada para trabalhar em diferentes âmbitos.*

- **Temperatura:**

  ![função de temperatura](assets/img%20-%20função%20necessária%20para%20temperatura.png)

  *Para esta função de temperatura, a biblioteca já trabalha para o sensor captar a temperatura ambiente (sem necessidade de intervenção).*

## Requisitos

Para a implementação e execução do código do protótipo (pasta `src`) no Arduino IDE, é necessária a prévia instalação das bibliotecas dos sensores (pasta `libraries`):

- [Instalação de bibliotecas no Arduino IDE](https://docs.arduino.cc/software/ide-v1/tutorials/installing-libraries/)
- [Instalação do Arduino IDE](https://www.arduino.cc/en/software)

Para a construção do protótipo, serão necessários:

| Qtd. | Componente |
|---|---|
| 1 | Cabo USB para Arduino Uno |
| 1 | Arduino Uno R3 ([documentação](https://docs.arduino.cc/hardware/uno-rev3/)) |
| 1 | LCD (Liquid Crystal Display) 16x2 ([documentação](https://docs.arduino.cc/learn/electronics/lcd-displays/)) |
| 1 | Sensor de temperatura TMP36 ([documentação](https://www.analog.com/media/en/technical-documentation/data-sheets/TMP35_36_37.pdf)) |
| 1 | Sensor de gás MQ-135 ([documentação](https://www.winsen-sensor.com/d/files/manual/mq135.pdf)) |
| 1 | Buzzer piezoelétrico ativo de 5V ([documentação](https://wiki-content.arduino.cc/documents/datasheets/PIEZO-PKM22EPPH4001-BO.pdf)) |
| 1 | Resistor de 330 Ω |
| 1 | Resistor de 1 kΩ |
| 1 | Resistor de 4 kΩ |
| 1 | Placa de ensaio (de preferência com 830 pontos) |
| 26 | Cabos jumper macho-macho (contados com a placa de ensaio incluída) |

## Observações

- O código do simulador e o do protótipo são diferentes.
- Os preços dos componentes do simulador estão sujeitos a valorização ou desvalorização.
- A escala termométrica utilizada em ambos os projetos é Celsius (ºC).
- O protótipo deve ser utilizado para propósitos experimentais. Seu uso não é recomendado em projetos profissionais ou que envolvam segurança humana ou ambiental.
- Os sensores, cabos, resistores e circuitos correm risco de quebra ou queima se em contato direto com a água. Uma vez que o protótipo se encontra confinado em um recipiente transparente, é possível captar a temperatura da água, mas não gases.

---

## Tecnologias

[![Arduino](https://img.shields.io/badge/Arduino-00979D?style=flat-square&logo=arduino&logoColor=white)](https://www.arduino.cc)
[![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)](https://isocpp.org)
[![Tinkercad](https://img.shields.io/badge/Tinkercad-1477D1?style=flat-square&logo=tinkercad&logoColor=white)](https://www.tinkercad.com)

---

## Referências

| # | Referência | Aplicação no projeto |
|---|---|---|
| 1 | [UNEP — Gases de efeito estufa estão privando nossos oceanos de oxigenação](https://www.unep.org/pt-br/noticias-e-reportagens/reportagem/gases-de-efeito-estufa-estao-privando-nossos-oceanos-de) | Impacto dos gases nos oceanos |
| 2 | [Iberdrola — A acidificação dos oceanos: por que ocorre e quais são as suas consequências?](https://www.iberdrola.com/sustentabilidade/acidificacao-oceanos) | Escolha do CO2 como gás monitorado |
| 3 | [Gizmodo — Temperatura dos oceanos quebrou recorde todos os dias em um ano](https://gizmodo.uol.com.br/temperatura-dos-oceanos-quebraram-recorde-todos-os-dias-em-um-ano/) | Medição da temperatura da superfície |
| 4 | [Vaisala — Como medir o dióxido de carbono](https://www.vaisala.com/sites/default/files/documents/VIM-G-How-to-measure-CO2-Application-Note-B211228PT.pdf) | Faixa de ppm do sensor MQ-135 |
