En el DER las _relaciones_ se las representa por la línea que ves entre las tablas. 

1. La patita sola | indica de qué lado está ese único elemento que se relaciona con el resto.
2. Las tres patitas nos dicen dónde están los “muchos” elementos que se relacionan con alguien del otro lado. 
3. Se suelen poner dos de estos elementos de cada lado, indicando la cantidad mínima y la máxima. 

En el ejemplo de las canciones se leería así: 

* Una canción se relaciona (tiene) con une y solo une artista. Ojo: pueden haber varias canciones que compartan le misme artista.
* Une artista se relaciona (tiene) con muchas canciones.  

> ¿Cómo se leería la siguiente relación?

<div
  class='mu-erd'
  data-entities='{
    "madres": {
      "id_madre": {
        "type": "Integer",
        "pk": true
      },
      "nombre_madre": {
        "type": "Text"
      }
    },
    "hijes": {
      "id_hije": {
        "type": "Integer",
        "pk": true
      },
      "nombre_hije": {
        "type": "Text"
      },
     "id_madre": {
        "type": "Integer",
        "pk": false,
        "fk": {
          "to": { "entity": "madres", "column": "id_madre" },
          "type": "many_to_one"
        }
      }
    }
  }'>
</div>

