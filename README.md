# 3D Printer Core H4 - GTmax

Este repositório armazena os G-codes inicial e final de fábrica da Impressora 3D Core H4 da GTmax.</br>
Os códigos são utilizados para realizar a configuração da impressora no _software_ UltiMaker Cura, entre outros.

## G-code
* G-code Inicial

```
G28; HOME GERAL
M400
G29 V4 T; AUTO NIVELAMENTO
M400
G1 X-8 Y100 Z0.8 F3000; VAI PARA PONTO DE PURGA
G92 E0; RESETA EXTRUSOR
G1 E30 F200; PURGA FILAMENTO
G92 E0;  RESETA EXTRUSOR
G1 E-3; RETIRA PRESSAO DO BICO
G1 Z1 F3000;
G1 X10 Y10 Z0.3 F3000; MOVIMENTO PRA SOLTAR PURGA
G1 X0 Y30 Z1 F10000; MOVIMENTO PRA SOLTAR PURGA
G1 X10 Y10 Z0.3 F10000; MOVIMENTO PARA SOLTAR PURGA
G1 Z5 F3000
```

* G-code Final
```
M107 ; DESLIGA FAN
G1 X-8
G1 Y100
G1 Z 445
M104 S0 ; DESLIGA AQUECIMENTO BICO
M140 S0 ; DESLIGA AQUECIMENTO MESA
M84 ; DESLIGA MOTORES
M300 S4 P1000 ; GERA BEEP
```

## Perfis
Os perfis de fábrica também estão disponíveis [Clique Aqui](https://github.com/mannalab/3D_Printer_Core_H4/tree/main/Perfis).

* Filamento ABS
* Filamento PLA
* Filamento PETG
* Filamento Flexivel
* Filamento Tritan