# GitHub

## 1. Conectar a Github

### 1.1 Generar Clave SSH

```bash
$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

> Sustituir la dirección de correo electrónico que tiene registrado en GitHub.

Cuando le pregunte si desea almacenar la clave en la ruta prederterminada, oprime Enter para aceptar, a continuación, le pedira una contraseña segura.

### 1.2 Agregar Clave SSH al ssh-agent

SSH-Agent permite recordar mientras dure la sesión, cada una de las claves privadas del usuario, de modo que él se encargue de realizar la autenticación. 

1. Inicia el agente SSH en segundo plano:

```bash
$ eval "$(ssh-agent -s)"
```

2. Agrega tu llave privada SSH al ssh-agent:

```bash
$ ssh-add ~/.ssh/id_rsa
```
### 1.3 Agregar la llave pública a GitHub

La llave pública se encuentra en:

```bash
cat ~/.ssh/id_rsa.pub
```
