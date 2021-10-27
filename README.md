# Guía Verilog

## Programación estructural

Ejemplificaremos con un semisumador.Construiremos el semisumador utilizando componentes más simples y describiendo cómo estos componentes se conectan internamente para, a partir de las señales de entrada, proporcionarnos las señales de salida.

'''
//Semisumador de dos entradas de 1 bit realizado a partir de puertas
module ha_v1(output wire sum, output wire carry, input wire a, input wire b);
//Declaración de conexiones o variables internas: no hay ninguna
//Estructura interna: Instancias de puertas y sus conexiones
xor xor1(sum, a, b);
and and1(carry, a, b);
endmodule
'''

Una vez que definamos el bloque o módulo semisumador, podremos usarlo para construir otros bloques más complejos.

'''
module pepe(...)
...
ha_v1 mi_semisumador(suma, acarreo, op1, op2);
...
endmodule
'''

## Bancos de prueba (testbenches)

