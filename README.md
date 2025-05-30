# Monitoramento de Pacientes com Doença Crônica

Descrição:
* Neste tutorial, vamos desenvolver um sistema de monitoramento de sinais vitais para pacientes com doenças crônicas, utilizando um ESP32 e sensores biomédicos para medição de temperatura e frequência cardíaca. O sistema enviará os dados coletados para um servidor na nuvem, permitindo o acompanhamento remoto por profissionais de saúde e familiares.

## Índice

1. Introdução

2. Requisitos

3. Configuração do Ambiente

4. Montagem do Circuito

5. Programação

6. Teste e Validação

7. Expansões e Melhorias

8. Referências

# Introdução

* Pacientes com doenças crônicas, como hipertensão e diabetes, precisam de monitoramento contínuo para evitar complicações. Este projeto propõe um sistema de monitoramento IoT que permite a coleta de dados vitais e o envio dessas informações para a nuvem, possibilitando um acompanhamento remoto eficiente.

# Requisitos

## Hardware

* Placa: ESP32
* Sensores: MAX30102 (oxímetro e frequência cardíaca), DHT11 (temperatura e umidade)
* Atuadores: LED de alerta, buzzer
* Outros componentes: Jumpers, resistores, protoboard

## Software
* Linguagem: C++ para ESP32
* IDE: Arduino IDE

* Bibliotecas: Wire.h, Adafruit_Sensor.h, DHT.h, MAX30102.h

# Configuração do Ambiente

## Passo 1: Instalação do Software

* Instalar Arduino IDE e configurar a placa ESP32.
* Adicionar bibliotecas necessárias na Arduino IDE:

#include <Wire.h>
#include <Adafruit_Sensor.h>
#include <DHT.h>
#include <MAX30102.h>

## Passo 2: Configuração da Placa ESP32

* Conectar a placa ao computador e selecionar a porta correta.
* Carregar um código de teste para verificar a comunicação.
* Montagem do Circuito
* MAX30102: Conectar os pinos SDA e SCL ao ESP32.
* DHT11: Conectar ao pino digital definido no código.
* LED e Buzzer: Conectar aos pinos GPIO apropriados.

Nota: Utilizar um diagrama de conexão para melhor compreensão.

# Programação

## Passo 1: Configuração dos Sensores

![image](https://github.com/user-attachments/assets/2e269758-2ec5-45e2-aede-f757e19e0dd3)

## Passo 2: Envio dos Dados para a Nuvem

Para enviar os dados para a nuvem, utilizaremos o protocolo MQTT  o Firebase como plataforma de armazenamento.

* Implementar conexão Wi-Fi e envio via MQTT/Firebase.

![image](https://github.com/user-attachments/assets/0abdac3a-4731-4a54-a5a1-77468ccdab49)

* 1ª caso, envio dos Dados para Firebase.

![image](https://github.com/user-attachments/assets/584a2807-e0e7-48ec-8766-d19f023d2935)

* 2ª caso, envio via MQTT.
  
![image](https://github.com/user-attachments/assets/04ab94d1-df31-4acf-8475-cb30fe9d43d4)


# Teste e Validação
* Verificar sensores com leitura via Serial Monitor.
* Testar alertas acionando LED/buzzer conforme limites definidos.
* Validar envio para a nuvem acessando os dados remotamente.

# Expansões e Melhorias
* Criar um dashboard web para monitoramento remoto.
* Implementar notificação via app ou SMS.
* Adicionar outros sensores, como pressão arterial.

# Referências
* Documentação da biblioteca Adafruit_Sensor
* Guia de configuração do ESP32 no Arduino IDE
* Introdução ao protocolo MQTT para IoT

