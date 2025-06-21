# FIAP - Faculdade de Informática e Administração Paulista

<p align="center">
<a href= "https://www.fiap.com.br/"><img src="assets/logo-fiap.png" alt="FIAP - Faculdade de Informática e Admnistração Paulista" border="0" width=40% height=40%></a>
</p>

<br>

# Atividade FASE4_CAP1 - FARMTECH

## 👨‍🎓 Integrantes: 
- Carlos Daniel Silveira Do Nascimento - RM88439
- Mauricio Jose Ferlin Tonnera - RM565469
- Rodrigo Portugal Santos - RM564773

## 👩‍🏫 Professores:
### Tutor
- Leonardo Ruiz Orabona
### Coordenador
- André Godoi


## 📜 Descrição

Este projeto tem como objetivo criar um sistema de monitoramento de sensores em plantações, permitindo o registro e acompanhamento de leituras como umidade, fósforo e potássio do solo. A arquitetura é composta por:

- ESP32 com sensores físicos (simulados)

- Script em Python com SQLite (armazenamento dos dados)

> Este projeto é baseado na versão da Fase 3 da FarmTech Solutions, agora reestruturado conforme o template oficial.

## 🎥 Vídeo de Demonstração

Vídeo com o código em funcionamento: https://youtu.be/yiYGIzw4ZB8


## 📁 Estrutura de pastas

Dentre os arquivos e pastas presentes na raiz do projeto, definem-se:

- <b>.github</b>: Nesta pasta ficarão os arquivos de configuração específicos do GitHub que ajudam a gerenciar e automatizar processos no repositório.

- <b>assets</b>: aqui estão os arquivos relacionados a elementos não-estruturados deste repositório, como imagens.

- <b>config</b>: Posicione aqui arquivos de configuração que são usados para definir parâmetros e ajustes do projeto.

- <b>document</b>: aqui estão todos os documentos do projeto que as atividades poderão pedir. Na subpasta "other", adicione documentos complementares e menos importantes.

- <b>scripts</b>: Posicione aqui scripts auxiliares para tarefas específicas do seu projeto. Exemplo: deploy, migrações de banco de dados, backups.

- <b>src</b>: Todo o código fonte criado para o desenvolvimento do projeto ao longo das 7 fases.

- <b>README.md</b>: arquivo que serve como guia e explicação geral sobre o projeto (o mesmo que você está lendo agora).

## 🔧 Como executar o código

### Simulação ESP32 no Wokwi
✅ Como Acessar:
Abra o projeto clicando [Aqui](https://wokwi.com/projects/434219114256049153)

✅ Componentes Usados:
- ESP32
- Sensor DHT22 (umidade)
- Fotoresistor (simula pH)
- Botões (fósforo e potássio)
- Display LCD I2C
- Serial Plotter (gráfico de variáveis)

💡 O que faz?
- Lê sensores e exibe em tempo real no LCD
- Liga a bomba se a umidade < 40%
- Mostra dados em gráfico pelo Serial Plotter
- Código comentado e otimizado para memória

## 🗃 Histórico de lançamentos

* 0.5.0 - XX/XX/2024
    * 
* 0.4.0 - XX/XX/2024
    * 
* 0.3.0 - XX/XX/2024
    * 
* 0.2.0 - XX/XX/2024
    * 
* 0.1.0 - XX/XX/2024
    *

## 📋 Licença

<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"><p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/agodoi/template">MODELO GIT FIAP</a> por <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://fiap.com.br">Fiap</a> está licenciado sobre <a href="http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">Attribution 4.0 International</a>.</p>
