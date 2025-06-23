# Ejemplo de TDD en PHP: Login Básico con PHPUnit

Este repositorio contiene un ejemplo básico de desarrollo guiado por pruebas (TDD) en PHP. Se implementa un sistema de autenticación simple con sus respectivas pruebas unitarias utilizando PHPUnit.

## Estructura
```bash
.
├── src/
│ └── LoginService.php
├── tests/
│ └── LoginTest.php
├── phpunit.xml
└── README.md

```


## 1. Instalación

1. Clona este repositorio:
   ```bash
   git clone https://github.com/tuusuario/ejemplo-login-tdd.git
   cd ejemplo-login-tdd
   ```
Instala las dependencias con Composer:

```bash

composer require --dev phpunit/phpunit
```
2. LoginService (Código de Producción)
```php

// src/LoginService.php

<?php

class LoginService
{
    private $usuarios = [
        'usuario' => 'clave123',
    ];

    public function autenticar($usuario, $clave)
    {
        return isset($this->usuarios[$usuario]) && $this->usuarios[$usuario] === $clave;
    }
}
```
3. LoginTest (Pruebas con PHPUnit)
```php
// tests/LoginTest.php

<?php

use PHPUnit\Framework\TestCase;
require_once __DIR__ . '/../src/LoginService.php';

class LoginTest extends TestCase
{
    public function testLoginCorrecto()
    {
        $login = new LoginService();
        $this->assertTrue($login->autenticar('usuario', 'clave123'));
    }

    public function testLoginIncorrecto()
    {
        $login = new LoginService();
        $this->assertFalse($login->autenticar('usuario', 'claveIncorrecta'));
    }
}
```
4. Ejecutar las pruebas
```bash
./vendor/bin/phpunit tests
```
5. Resultado esperado
```vbnet
PHPUnit x.y.z by Sebastian Bergmann and contributors.
```
..                                                                  2 / 2 (100%)

Time: 00:00.123, Memory: 6.00 MB

OK (2 tests, 2 assertions)
6. ¿Qué demuestra este proyecto?
Aplicación de TDD: primero se escribe el test, luego el código mínimo para pasarlo.

Separación de lógica de negocio y pruebas.

Uso de PHPUnit como framework de testing.

7. Próximos pasos sugeridos
Introducir inyección de dependencias.

Simular una base de datos o almacenamiento real.

Agregar pruebas de integración.


