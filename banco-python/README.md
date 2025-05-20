# Entrega 2: Armazenamento de Dados em Banco SQL com Python

## Objetivo

Esta entrega tem como foco simular o armazenamento dos dados capturados por sensores (como umidade, fósforo e potássio) em um banco de dados relacional, utilizando Python com SQLite. As operações CRUD foram implementadas, e o modelo relacional segue a estrutura definida no MER da Fase 2.

---

## Contexto e Simulação

Os dados utilizados representam leituras que, em um cenário real, seriam coletadas via monitor serial do ESP32. No entanto, como o circuito está hospedado no [Wokwi](https://wokwi.com), sem um microcontrolador físico conectado, optou-se por **simular a coleta desses dados diretamente no script Python**, conforme permitido na proposta da entrega.

---

## Estrutura das Tabelas e Relação com o MER

As tabelas abaixo foram criadas no script `main.py` com base nas entidades definidas no MER (com as correções aplicadas conforme a atividade da fase 2):

### T_SENSOR
| Campo              | Tipo         | Descrição                                      |
|-------------------|--------------|-----------------------------------------------|
| ID_SENSOR         | INTEGER PK   | Identificador único do sensor                 |
| TIPO              | TEXT         | Tipo do sensor (ex: umidade, fósforo, etc.)   |
| STATUS            | TEXT         | Estado atual do sensor (ativo/inativo)        |
| DATA_INSTALACAO   | TIMESTAMP    | Data de instalação do sensor                  |
| ID_PLANTACAO      | INTEGER FK   | Chave estrangeira para a plantação associada  |

### T_LEITURA_SENSOR
| Campo              | Tipo         | Descrição                                      |
|-------------------|--------------|-----------------------------------------------|
| ID_LEITURA        | INTEGER PK   | Identificador da leitura                      |
| DATA_HORA         | TIMESTAMP    | Data e hora da leitura                        |
| VALOR             | DOUBLE       | Valor quantitativo lido pelo sensor           |
| TIPO_MEDICAO      | TEXT         | Tipo da medição (umidade, fósforo, potássio)  |
| ID_SENSOR         | INTEGER FK   | Sensor associado                              |

---

## Funcionalidades do Script

O arquivo `main.py` contém as seguintes funcionalidades:

- **Inserção de dados simulados**, como se tivessem sido capturados pelo ESP32.
- **Consulta das leituras** por tipo ou por sensor.
- **Atualização de valores** ou tipo de medição.
- **Remoção de registros** de leitura específicos.
- **Criação e reset do banco** SQLite para testes.

---

## Exemplos de Dados Inseridos

```plaintext
Leitura 1: Umidade - 45.2%
Leitura 2: Fósforo - 18.7 ppm
Leitura 3: Potássio - 25.0 ppm
