# Transbank OpenCart 3.x Webpay Plugin

## Description

This OpenCart 3.x plugin implements
The [SDK PHP of Transbank] (https://github.com/transbankdevelopers/transbank-sdk-php)

## Dependencies

* Transbank / Transbank-SDK (Composer)
* FPDF.


## Installing the plugin for a trade

The Installation Manual for the End User is available [ACÁ] (DOCS / INSTALLATION.MD) OR
in pdf [here] (https://github.com/transbankdevelopers/transbank-plugin-opencart-webpay/blob/master/docs/installation.pdf)


## Note
- The PHP SDK version is found in the file `config.sh` and
In `SRC / Upload / System / Library / Transbank / Composer.json`

** Note: ** The version of the PHP SDK is located in the Script Config.sh

## Prepare the project to download Dependencies

    ./config.sh.

## Create a version of the packaged plugin

    ./package.sh.

## Developing

To support the rapid uprising of a development environment, we have created the specification of containers a
through Docker Compose.

To use it follow the following [Readme OpenCart 3.x] (./ Docker-OpenCart3)

### Update the installation PDF
Install `MarkDown-PDF` with` NPM I -G MarkDown-PDF` and then to generate the file `Installation.pdf` be it must run:
```
CD docs /
MarkDown-PDF Installation.md
```

Generate a new version

To generate a new version, you must create a PR (with a "Prepare Release X.Y.Z" title with the values ​​that correspond to X, Y and Z). The SEMVER standard must be followed to determine if the X value is increased (if there are non-recompatible changes), and (for retractionable improvements) or Z (if there were only bugs corrections).

In that PR the following changes should be included:

    Modify the CHANGELOG.MD file to include a new entry (at the beginning) for x.y.z to explain the changes in Spanish.

After obtaining approval from the Pull Request, you must mix Master and immediately generate a github release with the Tag vx.y.z. In the release description you must put the same as you added to the Changelog.

With that travis CI will automatically generate a new version of the plugin and update the GitHub release with the plugin zip.

    © 2021 Github, Inc.
    TERMS.
    Privacy
    SECURITY.
    Status
    Docs.

    Contact Github.
    Pricing
    API.
    Training
    Blog
    
---------

# Transbank Opencart 3.x Webpay Plugin

## Descripción

Este plugin de Opencart 3.x implementa 
el [SDK PHP de Transbank](https://github.com/TransbankDevelopers/transbank-sdk-php) 

## Dependencias

* transbank/transbank-sdk (composer)
* fpdf


## Instalación del plugin para un comercio

El manual de instalación para el usuario final se encuentra disponible [acá](docs/INSTALLATION.md) o 
en PDF [acá](https://github.com/TransbankDevelopers/transbank-plugin-opencart-webpay/blob/master/docs/INSTALLATION.pdf)


## Nota  
- La versión del sdk de php se encuentra en el archivo `config.sh` y 
en `src/upload/system/library/transbank/composer.json`

**NOTA:** La versión del sdk de php se encuentra en el script config.sh

## Preparar el proyecto para bajar dependencias

    ./config.sh

## Crear una versión del plugin empaquetado 

    ./package.sh

## Desarrollo

Para apoyar el levantamiento rápido de un ambiente de desarrollo, hemos creado la especificación de contenedores a 
través de Docker Compose.

Para usarlo seguir el siguiente [README Opencart 3.x](./docker-opencart3)

### Actualizar el PDF de instalación
Instalar `markdown-pdf` con `npm i -g markdown-pdf` y luego para generar el archivo `INSTALLATION.pdf` sea debe ejecutar: 
```
cd docs/
markdown-pdf INSTALLATION.md
```

## Generar una nueva versión

Para generar una nueva versión, se debe crear un PR (con un título "Prepare release X.Y.Z" con los valores que correspondan para `X`, `Y` y `Z`). Se debe seguir el estándar semver para determinar si se incrementa el valor de `X` (si hay cambios no retrocompatibles), `Y` (para mejoras retrocompatibles) o `Z` (si sólo hubo correcciones a bugs).

En ese PR deben incluirse los siguientes cambios:

1. Modificar el archivo `CHANGELOG.md` para incluir una nueva entrada (al comienzo) para `X.Y.Z` que explique en español los cambios.

Luego de obtener aprobación del pull request, debes mezclar a master e inmediatamente generar un release en GitHub con el tag `vX.Y.Z`. En la descripción del release debes poner lo mismo que agregaste al changelog.

Con eso Travis CI generará automáticamente una nueva versión del plugin y actualizará el Release de Github con el zip del plugin.
