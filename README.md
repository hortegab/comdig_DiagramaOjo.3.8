# INTRODUCCION
- Se trata de un paquete para python, gracias a lo cual vas a contar con una función que puedes usar en Python3 para graficar el diagrama de ojo a una señal representada en un vector.
- El desarrollo le pertenece a Warren Weckesser y la versión original se encuentra justamente es us github: https://github.com/WarrenWeckesser/eyediagram
- Lo único nuevo que aportamos aquí es lo siguiente:
  -- damos instrucciones precisas para la instalación y explotación con python 3.8.2. Es un avance si se tiene en cuenta que la versión mencionada fue hecha con Python 2.7.
  -- Hemos pulidos los ejemplos y la explicación para comprabar su funcionamiento
  -- El proceso de instalación que brindamos aquí se orienta a que este paquete sea usado en GNU Radio version 3.8.1 en el OOT E3TRadio
  -- Las mejoras las hemos realizado solo con propósitos pedagógicos.

# LA INSTALACION
## Prerrequisitos (dependencias)
- Se supone que usted está siguiendo las instrucciones de instalación del OOT E3TRadio para GNU Radio 3.8 que aparecen en https://github.com/hortegab/comdig_Lib_OOT_E3TRadio.3.8. Entonces allí ya ha instalado las dependencias y no hay más prerequisitos.

## La instalación es tan simple como:
- Entra a la carpeta "Instalación" y desde allí abre el terminal de Ubuntu, envía el comando:/n
  sudo python3 setup.py install

# PRUEBAS
- Abre un terminal de comandos y envia lo siguiente:
  pip3 list
- Revisa la lista que aparece, donde deverá figurar eyediagram


# INSTRUCCIONES DE USO AVANZADO
## Introducción
- Si trabajas en GNU Radio, no necesitas hacer nada de lo que se explica aquí, porque todo está incluido en GNURadio através del OOT E3TRadio
- Pero si por alguna razón quieres entrar al detalle de este paquete, estas son las instrucciones

## Las instrucciones

demo_data(num_symbols, Sps): es una función que puedes usar desde python para generar una señal de prueba, para ser usada con la función que se explica más abajo. num_symbols: es el número de simbolos en esa señal: Sps: es el núemro de muestras por simbolo (Samples per simbol). Por ejemplo: y=demo_data(1000, 24) llenará el vector "y" con las muestras de una señal digital demostrativa, con 1000 simbolos y cada uno de a 24 muestras.

eyediagram(y, Ns*Sps, offset, graptool): grafica el diagrama de ojo de "y". A continuación, los parámetros que restan por explicar. Ns es el número simbolos que quisieras ver en un ojo;  offset: es un parámetro para desplazar el ojo en offset muestras; graptool: es un parámetro que el tipo de herramienta gráfica a usar entre las que se tienen en python. Esto se verá mejor en el ejemplo de abajo cuando se usa matplolib, pero la idea que que se puedan usar otras.

# Ejemplo de uso y de prueba con código en python3:
Un ejemplo de código en Pyhton3 se tiene en la carpeta Ejemplos/Para Python3/Ejemplo1.py

# Ejemplo de uso y de prueba con GNU Radio 3.8.1:
Hemos incluido un ejemplo para GNU Radio v 3.8.1, pero requiere que hayas concluido las instalación del OOT E3TRadio. Se encuentra en la carpeta Ejemplos/Para GNU Radio/Ejemplo2.grc. Hay que tener en cuenta que la adaptación realizada hasta el momento a GNU Radio no es completamente natural ya que no se usa graficas tipo QT, por ello el Diagrama de Ojo resulta ser persistente y solo se detiene cuando se detiene el flujograma

Si no estás satisfecho:
- tenemos un manual más completo en: https://es.overleaf.com/read/mxdwhbddzjhv
- tambien puedes acudir a la aplicación original en: https://github.com/WarrenWeckesser/eyediagram
