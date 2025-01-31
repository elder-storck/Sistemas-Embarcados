# README - Laboratório de Sistemas Embarcados

Este laboratório utiliza **Node-RED** e comunicação **MQTT** para interagir com um **broker**, possibilitando a troca de mensagens entre dispositivos IoT.

Foram utilizados os módulos **MQTT in** e **MQTT out** para envio e recebimento de mensagens, além do módulo **debug** para exibição dos resultados na tela. Também foram empregados módulos de **dashboard**, como o **gauge**, para visualização dos dados.

Uma função foi implementada para modificar um dos mostradores no **gauge**, realizando um tratamento nos dados recebidos. O código da função utilizada é:

```javascript
var info = msg.payload;
msg.payload = parseFloat(info.replace(/ /g, "").replace(":", "").replace(/^[zA-z]+/, ""));
return msg;
```
Mais detalhes sobre o projeto podem ser encontrados no arquivo PDF disponível.

A maquete do projeto está documentada nas fotos, assim como os prints do Node-RED demonstrando a configuração e funcionamento do sistema.
