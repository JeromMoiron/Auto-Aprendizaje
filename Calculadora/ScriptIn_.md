## Calculadora Avanzada

~~~bash
#! /bin/bash
# Este script crea unha calculadora mediante variables
separador="----------------------------------------------------------------"

sum=0
i=y
while [ $i = "y" ]
do 
echo "1.Sumar"
echo "2.Restar"
echo "3.Multiplicar"
echo "4.Dividir"
echo "Introduce el numero de operación seleccionada (1 al 4)"
echo "$separador"
echo "elija una función"
read ch
if [ $ch = 1 ]
then echo "Estas en Modo Suma"
fi
if [ $ch = 2 ]
then echo "Estas en Modo Resta"
fi
if [ $ch = 3 ]
then echo "Estas en Modo Multiplicación"
fi
if [ $ch = 4 ]
then echo "Estas en Modo División"
fi
echo "$separador"
echo "Introduce la primera cifra"
read n1
echo "Ahora la segunda"
read n2
echo "$separador"
case $ch in
    1)sum=`expr $n1 + $n2`
     echo "Resultado de la suma ="$sum;;
        2)sum=`expr $n1 - $n2`
     echo "Resultado de la resta = "$sum;;
    3)sum=`expr $n1 \* $n2`
     echo "Resultado de la multiplicación = "$sum;;
    4)sum=`expr $n1 / $n2`
     echo "Resultado de la división = "$sum;;
    *)echo "Tu selección es incorrecta";;
 esac
~~~

