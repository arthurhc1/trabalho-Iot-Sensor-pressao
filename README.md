# trabalho-Iot-Sensor-pressao
O trabalho tem como o propósito coletar dados de um sensor de pressão e 
enviá-lo para um cloud onde pode-se buscar a informação do que o sensor está lendo.
# Tecnologias utilizadas
- HiveMQ Cloud
link: https://console.hivemq.cloud/
- Wokwi
link: https://wokwi.com/
# Funcionamento
-no Wokwi: Possui um microcontrolador ESP32 no qual está ligado a um potenciômetro que 
simula um sensor, este sensor pode ser por exemplo de temperatura, 
também está conectado ao microcontrolador um resistor e um led, onde quando o sensor(potenciômetro) 
ler o valor 2000, ligará o led simulando um aviso analógico de um dispositivo por exemplo que pode
ser instalado em quarto para saber a temperatura dele e através de um aplicativo buscando
os tópicos do cloud HiveMQ, se saberá qual a temperatura do quarto. 
-no HiveMQ: Foi criado um servidor TLS onde através:
-porta: 8883
-host: 63d5c96356d24122987ae855f18860c7.s1.eu.hivemq.cloud
-user: esp32user
-senha: esp32pasS

utilizando os tópicos estufa/led e estufa/temperatura conseguimos acessar via cloud os valores lidos pelo sensor.
