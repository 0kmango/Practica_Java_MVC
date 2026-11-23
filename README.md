# Practica_Java_MVC

Proyectos de práctica de **Java con arquitectura MVC**, hechos durante las
clases y guardados como archivos comprimidos.

Cada proyecto es un **proyecto de NetBeans (Ant)**: incluye `build.xml`,
`nbproject/` y las clases ya compiladas en `build/classes/`. Las interfaces
están hechas con **Swing** (los archivos `.form` son del diseñador de NetBeans).

## Contenido

El contenido de cada comprimido fue verificado listando sus archivos; las
clases que aparecen son las que incluye el proyecto.

| Archivo | Proyecto | Paquetes y clases principales |
| :--- | :--- | :--- |
| `ColeccionCriaturasMVC.zip` | Registro de criaturas (dragones, hechiceros…) con vista Swing | `modelo` (`Criatura`, `Dragon`, `HechiceroOscuro`, `RegistroCriaturas`), `vista` (`VistaCriatura`) |
| `PersonajesSegunJuego.zip` | Personajes según el juego (proyecto NetBeans simple) | `personajessegunjuego` (`Main`) |
| `InterfazGrafica.rar` | Ejemplo base de interfaz gráfica con formularios de NetBeans | `interfazgrafica` (`Main`), `vista` (`HolaMundo`, `VistaPrincipal` + `.form`) |
| `MangosKiwis.rar` | Registro de frutas (mangos y kiwis) con cálculo de precios | `model` (`Fruta`, `Icalculable`), `dao` (`CRUD`, `FrutasDAOImpl`), `controlador`, `vista`, `persistencia` |
| `RegistroCancionesMVC.rar` | Registro de canciones | `model` (`Cancion`), `dao` (`CRUD`, `CancionesDAOimpl`), `controlador` (`ControladorCancion`), `vista` |
| `RegistroCute.rar` | Registro de personajes «cute» con imágenes | `model` (`ChicaCute`, `Tipo`), `dao` (`CuteDAOimpl`), `controlador` (`cuteControlador`) |
| `RegistroWarframesMVC.rar` | Registro de warframes con cálculo de estado Prime | `model` (`Warframe`, `Companhero`, `EstadoPrime`, `ICalculable`), `dao` (`ICRUD`, `WarframeDAOimpl`), `controlador`, `persistencia` |

## Cómo abrir un proyecto

1. Descomprimir:

   ```bash
   unzip ColeccionCriaturasMVC.zip

   # .rar (elige el que tengas):
   unar Archivo.rar          # Linux/macOS
   7z x Archivo.rar          # Linux/macOS
   # Windows: 7-Zip o WinRAR
   ```

2. **NetBeans** (recomendado): *File → Open Project* y seleccionar la carpeta
   descomprimida (contiene `build.xml`).
3. **IntelliJ IDEA / Eclipse**: importar el proyecto desde `src/` si prefieres
   no usar NetBeans.
4. Ejecutar la clase `Main` de cada proyecto desde el IDE.

## Requisitos

- **JDK 8 o superior** (`java -version`).
- **NetBeans** para aprovechar los `.form` del diseñador de interfaces.
- Un extractor de `.rar` (`unar`, `7z`, WinRAR o 7-Zip).

## Notas

- Los comprimidos incluyen `build/classes/` con el **bytecode compilado**. Si se
  recompila con otra versión de Java conviene borrar esa carpeta antes
  (`ant clean`), y en el repositorio lo ideal es versionar solo las fuentes:
  por eso el `.gitignore` excluye `build/`, `dist/` y `nbproject/private/`.
- Varios proyectos fueron entregas de clase, así que pueden estar incompletos.