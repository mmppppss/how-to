# README

El ejercicio de prueba es imprimir un mensaje en pantalla con el siguiente texto

    Hola Mundo



### Código

Crea un archivo llamado `holamundo.pas`

```pascal
program holamundo;
begin
    writeln('Hola Mundo');
end.
```

### Compilación

La compilación es bastante simple, solo es necesario ejecutar los siguientes comandos: 

    fpc holamundo.pas


### Ejecución

Para ejecutar el binario compilado, solo es necesario agregar `./` seguido del nombre del binario, asi:

    ./holamundo