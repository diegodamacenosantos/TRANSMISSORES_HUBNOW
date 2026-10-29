# TRANSMISSORES_HUBNOW

Firmwares dos sensores e atuadores que se comunicam com o [HUBNOW](https://github.com/diegodamacenosantos/HUBNOW) por **ESP-NOW**, usando o protocolo próprio **NWAY v3**. Cada arquivo é um sketch do Arduino: crie um sketch novo e cole o conteúdo.

Os transmissores para **ESP32** (padrão **ESP32-C3**) usam o core **esp32**. Os dois para **ESP8266** (`rele_sonoff_basic_rf_r2` e `disponibilidade_esp8266`) usam o core **esp8266**.

## Arquivos

| Arquivo | Para quê |
|---|---|
| `sensor_disponibilidade_esp32.txt` | sensor de disponibilidade: envia `ONLINE` ao hub enquanto está ligado e ao alcance (ESP32) |
| `sensor_disponibilidade_esp8266.txt` | o mesmo, para ESP8266 |
| `sensor_infravermelho_ky005_ky022.txt` | emissor e receptor infravermelho (KY-005 e KY-022): aprende e emite comandos |
| `sensor_infravermelho_ky005_ky022_teste.txt` | versão de teste do infravermelho |
| `sensor_luminosidade_ldr.txt` | luminosidade com LDR |
| `sensor_luminosidade_veml7700.txt` | luminosidade com o sensor VEML7700 |
| `sensor_on_off_generico.txt` | entrada liga/desliga genérica (0 ou 1) |
| `sensor_presenca_generico.txt` | sensor de presença genérico |
| `sensor_rele_generico.txt` | relé genérico, recebe `ON` e `OFF` |
| `sensor_rele_psf_b01.txt` | relé do modelo PSF-B01 |
| `sensor_rele_sonoff_basic_rf_r2.txt` | relé Sonoff Basic RF R2 (ESP8266) |
| `sensor_temperatura_umidade_dht11.txt` | temperatura, umidade e índice de calor (DHT11) |

## Como usar

1. Grave o firmware no transmissor.
2. Ligue o HUBNOW e o transmissor. Ele aparece no painel do HUBNOW, em **Dispositivos**.
3. Clique em **[ Aceitar ]** só no MAC desejado, edite nome, pinos e intervalo, e salve.

## Reset de um transmissor

Os transmissores não têm botão. Se o hub salvo sumir, depois de **5 minutos** sem resposta válida o transmissor abre uma rede aberta com o próprio **MAC** como nome, por **3 minutos**. Conecte e use o portal para fazer o **Reset**. Se não resetar, ele reinicia e volta a procurar o hub.