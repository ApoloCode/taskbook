<h1 align="center">
  Taskbook
</h1>

<h4 align="center">
  📓 Tareas, tableros y notas para la terminal de comandos.
</h4>

<div align="center">
  <img alt="Boards" width="60%" src="../media/header-boards.png"/>
</div>

<p align="center">
  <a href="https://travis-ci.com/klaussinani/taskbook">
    <img alt="Build Status" src="https://travis-ci.com/klaussinani/taskbook.svg?branch=master">
  </a>
</p>

## Presentación

Utilizando una simple y minimalista sintaxis, la cual hace la curva de aprendizaje menor, taskbook te permite gestionar eficientemente tus tareas y notas a traves de multiples tableros desde tu terminal. Toda la información es escrita automáticamente en archivos de almacenamiento para evitar la corrupción de estos y nunca son compartidos con alguien o algo. Elementos eliminados son automáticamente archivados y pueden ser inspeccionados o restaurados en cualquier momento.

Lee este documento en: [简体中文](https://github.com/klaussinani/taskbook/blob/master/docs/readme.ZH.md), [Русский](https://github.com/klaussinani/taskbook/blob/master/docs/readme.RU.md), [Français](https://github.com/klaussinani/taskbook/blob/master/docs/readme.FR.md), [Español](https://github.com/klaussinani/taskbook/blob/master/docs/readme.ES.md).

Visita la [guía de contribución](https://github.com/klaussinani/taskbook/blob/master/contributing.md#translating-documentation) para aprender como hacer la traducción de este documento en otros idiomas.

Ven a [Gitter](https://gitter.im/klaussinani/taskbook) o [Twitter](https://twitter.com/klaussinani) para compartir tus ideas sobre el proyecto.

## Ventajas

- Organizar tareas y notas en tableros
- Vista del tablero y de la linea de tiempo
- Mecanismos de prioridad y favoritos
- Buscar y filtar elementos
- Archivar y restaurar elementos eliminados
- Ligero y rápido
- Información escrita atómicamente en archivos de almacenamiento
- Localización customizable de los archivos de almacenamiento
- Visión general de progreso
- Sintaxis simple y minimalista
- Notificaciones de actualizaciones
- Configurable mediante `~/.taskbook.json`
- Información almacenada en un archivo JSON en `~/.taskbook/storage`

Imagenes de las ventajas en un [tablero taskbook](https://raw.githubusercontent.com/klaussinani/taskbook/master/media/highlights.png) en inglés.

## Contenido

- [Presentación](#presentación)
- [Ventajas](#ventajas)
- [Instalación](#instalación)
- [Uso](#uso)
- [Vistas](#vistas)
- [Configuración](#configuración)
- [Manual](#manual)
- [Development](#development)
- [Relacionado](#relacionado)
- [Equipo](#equipo)
- [Licencia](#licencia)

## Instalación

### Yarn

```bash
yarn global add taskbook
```

### NPM

```bash
npm install --global taskbook
```

### Snapcraft

```bash
snap install taskbook
snap alias taskbook tb # set alias
```

**Note:** coso

## Uso

```
$ tb --help

  Usage
    $ tb [<options> ...]

    Options
        none             Affiche la vue tableau
      --task, -t         Créé une tâche
      --note, -n         Créé une note
      --timeline, -i     Affiche la vue frise chronologique
      --delete, -d       Supprime une tâche ou une note
      --check, -c        Coche/décoche une tâche
      --star, -s         Ajoute aux favoris/Supprime des favoris une tâche ou une note
      --copy, -y         Copie la description d'une tâche ou d'une note
      --list, -l         Liste les tâches et les notes par attributs
      --find, -f         Cherche une tâche ou une note
      --edit, -e         Modifie la description d'une tâche ou d'une note
      --move, -m         Déplace une tâche ou une note entre des tableaux
      --priority, -p     Met à jour la priorité d'une tâche
      --archive, -a      Affiche les tâches et les notes qui sont archivées
      --restore, -r      Restaure les tâches et notes qui sont dans l'archive
      --clear            Supprime toutes les tâches et notes cochées
      --help, -h         Affiche le message d'aide
      --version, -v      Affiche la version de taskbook

    Examples
      $ tb
      $ tb --task Preparer de la creme glacee
      $ tb --task @coding Ameliorer la documentation
      $ tb --task @coding @reviews Revue PR #42
      $ tb --note @coding Trie avec fusion est dans le pire cas de complexite O(nlogn)
      $ tb --check 1 2
      $ tb --delete 4
      $ tb --star 2
      $ tb --copy 1 2 3
      $ tb --priority @3 2
      $ tb --timeline
      $ tb --edit @3 Fusionner PR #42
      $ tb --move @1 cuisinner
      $ tb --find documentation
      $ tb --list pending coding
      $ tb --archive
      $ tb --restore 4
      $ tb --clear
```

## Vistas

### Vista de tablero

Invocar taskbook sin ninguna opción desplegara todos los elementos guardados dentro de sus respectivos tableros.

<div align="center">
  <img alt="Boards" width="60%" src="../media/header-boards.png"/>
</div>

### Vista de la línea de tiempo

Despliega todos los elementos en orden en la vista de la línea del tiempo, basado en su fecha de creación, la opción `--timeline`/`-i` puede ser usada.

<div align="center">
  <img alt="Timeline View" width="62%" src="../media/timeline.png"/>
</div>

## Configuración

Para la configuración del taskbook ve al archivo `~/.taskbook.json` y modifica cualquiera de las opciones según tu propia preferencia. Para regresas a los valores predeterminados, simplemente elimina el archivo de configuración de tu directorio.

El siguiente ejemplo ilustra todas las opciones válidas con sus respectivos valores predeterminados.

```json
{
  "taskbookDirectory": "~",
  "displayCompleteTasks": true,
  "displayProgressOverview": true
}
```

### En detalle

#### `taskbookDirectory`

- Tipo: `String`
- Predeterminado: `~`

## Manual

## Desarrollo

Para más información sobre como contribuir al proyecto, favor de leer la [guía de contribución](https://github.com/klaussinani/taskbook/blob/master/contributing.md).

- Forkea el repositorio y clonalo en tu máquina.
- Navega hacia tu fork local: `cd taskbook`
- Instala las dependencias del proyecto: `npm install` o `yarn install`
- Prueba el código contra errores: `npm test` o `yarn test`

## Relacionado

- [signale](https://github.com/klaussinani/signale) - Affichage console hackable
- [qoa]() -
- [hyperocean]() - Tema de terminal

## Equipo

- Klaus Sinani [(@klaussinani)](https://github.com/klaussinani)
- Mario Sinani [(@mariosinani)](https://github.com/mariosinani)

## Licencia

[MIT](https://github.com/klaussinani/taskbook/blob/master/license.md)
