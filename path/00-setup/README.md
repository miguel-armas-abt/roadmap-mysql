# CONFIGURACIÓN

[← Regresar a notas](../../README.md) <br>

----

## ⚙️ Instalar MySQL
### Pre-requisitos:
- [Instalar Microsoft Visual C++ Redistributable](https://aka.ms/vs/17/release/vc_redist.x86.exe)

### Instrucciones:

[Descargar](https://dev.mysql.com/downloads/mysql/) `Windows (x86, 64-bit), ZIP Archive` y guardar los binarios en la ruta sugerida `C:\dev-environment\mysql\mysql-8.2.0`.
> 💻 Abrir una consola CMD en modo **<u>administrador</u>** e ingresar a los binarios
> ```shell
> cd bin
> ```

> 🔓 Inicializar la configuración de MySQL sin una contraseña por defecto para el usuario `root`
> ```shell
> mysqld --initialize-insecure
> ```

> ⚙️ Instalar MySQL80
> ```shell
> mysqld --install "mysql80"
> ```

> ▶️ Inciar el servicio
> ```shell
> net start mysql80
> ```

> 🔑 Inciar sesión sin contraseña
> ```shell
> mysql -u root
> ```

> 🔐 Establecer contraseña para el usuario `root`
> ```shell
> ALTER USER 'root'@'localhost' IDENTIFIED BY 'qwerty';
> ```

> ⏹️ Detener el servicio:
> ```shell
> net stop mysql80
> ```

> 👤 Inciar sesión con contraseña:
> ```shell
> mysql -u root -p"qwerty"
> ```

📌 **Nota**: Si necesitas repetir el proceso, asegúrate de eliminar los binarios y descargarlos nuevamente,
ya que estos podrían tener configuraciones obsoletas. Además, para desinstalar el servicio de MySQL puedes utilizar:
```shell
mysqld --remove "mysql80"
```
