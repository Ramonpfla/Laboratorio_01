# Laboratorio_01
ELF52 - Sistemas Microcontrolados
Ramon Percicotti Flauzino RA:1906925

Os Registros dos valores do código com MOV foram:
R0: 0x0000 0055 -> efetua a carga 0#0x55
R1: 0x0055 0000 -> shift para esquerda em 16 bits
R2: 0x0000 5500 -> shift para direita em 8 bits
R3: 0x0000 0550 -> shift aritmético para a direita em 4 bits
R4: 0x0000 0154 -> rotação para a direita em 2 bits
R5: 0x0000 00aa -> rotação com extensão para a direita

Durante a execução do programa foi possível observar o funcionamento das operações assim como acompanhar as mudanças passo a passo através das janelas Disassembly e Registers. Nessas janelas podemos acompanhar a posição do endereço da memória a cada parte executada, se as flags mudaram ou não (que nesse caso as flags não eram afetadas), as mudanças nos registros e também o endereço da próxima instrução através do PC. Nas operações é interessante obeservar as diferenças entre os operadores ROR e RRX, onde as duas operações fazem trabalhos similares mas o RRX leva em conta a flag C para fazer a rotação enquanto o ROR não.

Na segunda parte trocamos todos os MOV por MVN e os novos valores são:
R0: 0xffff'ffaa
R1: 0x0055'ffff
R2: 0xffff'aa00
R3: 0x0000'055f
R4: 0x3fff'fea8
R5: 0xe000'00ab

O MVN faz o trabalho de um not, ou seja, ele nega os bits da carga. Como exemplo, o valor hexadecimal do exercício que era de 0055 quando negado apresenta o valor ffaa. Nessa parte do exercício as outras operações continuaram as mesmas.
