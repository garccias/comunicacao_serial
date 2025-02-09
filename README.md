# 🚀 Projeto de Comunicação Serial com RP2040 e BitDogLab

## 📜 Descrição do Projeto

Este projeto tem como objetivo consolidar os conceitos sobre o uso de interfaces de comunicação serial no RP2040 e explorar as funcionalidades da placa de desenvolvimento BitDogLab. O projeto envolve a manipulação de LEDs comuns e LEDs endereçáveis WS2812, uso de botões de acionamento, interrupções e debounce, além de comunicação serial via UART e I2C.

## 🔧 Componentes Utilizados

- Matriz 5x5 de LEDs (endereçáveis) WS2812, conectada à GPIO 7.
- LED RGB, com os pinos conectados às GPIOs (11, 12 e 13).
- Botão A conectado à GPIO 5.
- Botão B conectado à GPIO 6.
- Display SSD1306 conectado via I2C (GPIO 14 e GPIO 15).

## 🎯 Funcionalidades do Projeto

1. **Modificação da Biblioteca `font.h`**
   - Adição de caracteres minúsculos à biblioteca `font.h`. Esta modificação permite que o display SSD1306 exiba tanto caracteres maiúsculos quanto minúsculos.

2. **Entrada de Caracteres via PC**
   - Utilização do Serial Monitor do VS Code para digitar caracteres.
   - Cada caractere digitado no Serial Monitor é exibido no display SSD1306.
   - Quando um número entre 0 e 9 é digitado, um símbolo correspondente ao número é exibido na matriz 5x5 WS2812.

3. **Interação com o Botão A**
   - Pressionar o botão A alterna o estado do LED RGB Verde (ligado/desligado).
   - A operação é registrada de duas formas:
     - Uma mensagem informativa sobre o estado do LED é exibida no display SSD1306.
     - Um texto descritivo sobre a operação é enviado ao Serial Monitor.

4. **Interação com o Botão B**
   - Pressionar o botão B alterna o estado do LED RGB Azul (ligado/desligado).
   - A operação é registrada de duas formas:
     - Uma mensagem informativa sobre o estado do LED é exibida no display SSD1306.
     - Um texto descritivo sobre a operação é enviado ao Serial Monitor.

## 📋 Requisitos do Projeto

1. **Uso de Interrupções**
   - Todas as funcionalidades relacionadas aos botões são implementadas utilizando rotinas de interrupção (IRQ).

2. **Debouncing**
   - Implementação do tratamento do bouncing dos botões via software.

3. **Controle de LEDs**
   - O projeto inclui o uso de LEDs comuns e LEDs WS2812, demonstrando o domínio de diferentes tipos de controle.

4. **Utilização do Display 128 x 64**
   - A utilização de fontes maiúsculas e minúsculas demonstra o domínio do uso de bibliotecas, o entendimento do princípio de funcionamento do display, bem como a utilização do protocolo I2C.

5. **Envio de Informação pela UART**
   - Visa observar a compreensão sobre a comunicação serial via UART.

6. **Organização do Código**
   - O código está bem estruturado e comentado para facilitar o entendimento.

## 📂 Estrutura do Código

### `numbers.h`
Contém as representações dos números de 0 a 9 usando a matriz 5x5 de LEDs.

### fonte.h
Modificado para incluir caracteres minúsculos, permitindo a exibição de uma gama mais ampla de caracteres no display SSD1306.

### serial.c
Implementa as funcionalidades descritas acima, incluindo a manipulação de LEDs, botões e display. Utiliza interrupções para detectar a pressão dos botões e debounce para garantir leituras estáveis.

🎥 [Demonstração](https://drive.google.com/file/d/1MHSUuecOA-a4oHleYUZzWbQ0qhRKF1pj/view?usp=sharing)


