🧪 Ejemplo de TDD con PHPUnit – Login básico
Paso 1: Escribir el test
'''php
// tests/LoginTest.php
use PHPUnit\Framework\TestCase;
require_once 'LoginService.php';

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
        $this->assertFalse($login->autenticar('usuario', 'claveErronea'));
    }
}
'''
Paso 2: Escribir el código mínimo para pasar el test
'''php

// LoginService.php
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
'''
Paso 3: Refactorizar (opcional)
Si el sistema crece, podrías usar clases como UserRepository, inyección de dependencias, etc.
