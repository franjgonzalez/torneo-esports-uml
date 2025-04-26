# Sistema de Gestión de Torneos de eSports

## Autor
!Nombre: Francisco José Juan González 
!Perfil de GitHub: https://github.com/franjgonzalez

## Descripción del Proyecto
Este proyecto implementa un sistema de gestión de torneos de eSports.
Se centra en la elaboración de diagramas UML para el modelado estructural y funcional del sistema.

Repositorio del proyecto: https://github.com/franjgonzalez/torneo-esports-uml

## Diagramas UML

### Diagrama de Casos de Uso
!(diagrams/casos-uso.png)

### Diagrama de Clases
!(diagrams/clases.png)

## Estructura del Proyecto
```
torneo-esports-uml/
├── src/
│   ├── es/empresa/torneo/
│   │   ├── entidad/
│   │   ├── control/
│   │   ├── interfaz/
│   │   ├── Main.java
├── diagrams/
│   ├── casos_uso.puml
│   ├── diagrama_clases.puml
├── README.md
├── .gitignore
```

## Instalación y Ejecución
1. Clonar el repositorio:
```bash
git clone https://github.com/tu_usuario/torneo-esports-uml.git
```

2. Compilar y ejecutar el proyecto:
```bash
cd src
javac es/empresa/torneo/Main.java
java es.empresa.torneo.Main
```

## Justificación del Diseño

### Diagrama de Casos de Uso
Se han identificado tres actores principales: Administrador, Jugador y Sistema. El administrador puede registrar equipos, añadir jugadores y consultar la lista de equipos/jugadores. Los jugadores solo pueden consultar. Se ha utilizado la relación `<<include>>` entre "Añadir jugadores a un equipo" y "Registrar equipo", ya que no se pueden añadir jugadores sin un equipo previamente registrado.

### Diagrama de Clases
Se ha organizado el sistema en tres capas:
- **Entidad**: Clases que representan los datos del sistema (`Equipo`, `Jugador`, `Torneo`).
- **Control**: Clase `GestorEquipos` que gestiona las operaciones principales.
- **Interfaz**: Clase `VistaPrincipal` que muestra la información a los usuarios.

Se utilizan relaciones de agregación (`o--`) para representar que un equipo contiene varios jugadores y un torneo contiene varios equipos. Se aplicó también principios de encapsulamiento y modularidad para separar responsabilidades.

## Conclusiones
Se ha practicado el modelado de sistemas utilizando UML, identificando actores, casos de uso, clases y sus relaciones. Es una buena tarea para practicar la elaboración de diagramas de clases utilizados en Programación Orientada a Objetos.
