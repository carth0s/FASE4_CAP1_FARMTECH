# Sistema de Irrigação Automatizado com Monitoramento de Nutrientes

## Descrição do Projeto
Este projeto simula um sistema inteligente de irrigação utilizando sensores físicos e digitais para monitorar a umidade do solo e a presença de nutrientes (fósforo e potássio), acionando automaticamente uma bomba de irrigação quando necessário.
Foi desenvolvido com base em uma placa ESP32, utilizando o simulador Wokwi.

## Componentes Utilizados

- ESP32 - Microcontrolador principal
- DHT22	Sensor digital de temperatura e umidade (usado aqui apenas para umidade)
- LDR (simula pH)	Sensor analógico utilizado como simulação de leitura de pH
- Botões	Simulam presença de fósforo e potássio no solo
- LED	Simula o relé de acionamento de uma bomba de irrigação

## Funcionalidades
- Leitura da umidade com o sensor DHT22.
- Leitura analógica simulada do pH via um LDR.
- Detecção de nutrientes: dois botões simulam presença de fósforo e potássio.
- Acionamento automático da bomba:
  - A bomba liga (LED acende) apenas se a umidade for inferior a 40%.
  - A ausência de nutrientes não aciona a bomba, mas emite alertas no monitor serial.
- Monitor serial exibe todas as leituras e alertas.

## Lógica de Funcionamento

```cpp
  if (umidade < 40.0) {
    // Liga bomba se solo estiver seco
  }

  if (!fosforo) {
    // Alerta de falta de fósforo
  }

  if (!potassio) {
    // Alerta de falta de potássio
  }
```
A lógica foi pensada para irrigar o solo quando a umidade estiver a baixo de 40%, e monitorar a presença/ausência de fósforo e potácio no solo.

## Leitura no Monitor Serial
Exemplo de saída no monitor serial:
```yaml
  Alerta: Falta de fósforo no solo.
  ----- LEITURAS -----
  Umidade: 35.40
  pH (simulado com LDR): 846
  Fósforo (botão): 0
  Potássio (botão): 1
```
## Plataforma Utilizada
Wokwi Simulator: Link para o projeto https://wokwi.com/projects/431422752922568705

## Imagem do Circuito
Insira aqui um print ou foto do circuito montado no Wokwi.

## Observações Finais
O código foi comentado de forma didática para facilitar a leitura e a avaliação.

