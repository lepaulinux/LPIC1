💻 Comandos para Investigar o Hardware
Comandos essenciais para identificar e analisar o hardware no Linux.
```
# Listar Dispositivos USB
lsusb 
```
Função
Lista dispositivos conectados via USB:
- Mouse
- Teclado
- Webcam
- Pen drives
Exemplos
```
lsusb
```
Detalhes técnicos de um dispositivo específico:
```
lsusb -v -d ID_DO_DISPOSITIVO
```
Visualização em árvore (topologia USB):
```
lsusb -t
```

```
# Listar Dispositivos PCI
lspci
```
Função
Lista dispositivos conectados ao barramento PCI:
- Placas de vídeo
- Placas de rede
- Controladoras de som
Exemplos
Listagem simples:
```
lspci
```
Detalhes de um dispositivo específico:
```
lspci -v -s ENDEREÇO
```
Verificar o driver (módulo do kernel) em uso:
```
lspci -k -s ENDEREÇO
```

📌 Dica importante:
Este comando mostra exatamente qual driver do kernel está associado ao hardware.
```
# Listar Módulos do Kernel
lsmod
```
Exibe todos os módulos (drivers) atualmente carregados no kernel.
Exemplo:
```
# Listar todos os módulos:
lsmod
```
Verificar se um driver específico está ativo (ex: placa de vídeo Intel):
```
lsmod | grep i915
```

🔗 Relação entre os comandos
```
lspci -k 
# identifica qual driver o hardware usa
```

```
lsmod 
# confirma se esse driver está carregado
```

