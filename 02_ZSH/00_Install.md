# ZSH

Es un interprete de comandos para sistemas operativos de tipo Unix.

## 1. Instalación de ZSH y git

```bash
sudo apt install zsh git
```

# Antigen

Antigen es un conjunto de funciones que ayudan a administrar fácilmente los plugins de zsh.

## 1. Instalación

```bash
curl -L git.io/antigen > antigen.zsh
``` 

## 2. Configuración

Se deben seguir los siguientes pasos: 

### 1. Abrir el fichero de configuración `.zshrc` con un editor:

```bash
vim  ~/.zshrc
```

### 2. Se copian las siguiente líneas:

```bash
# Linux antigen file
source /usr/share/zsh-antigen/antigen.zsh

# Load the oh-my-zsh's library.
antigen use oh-my-zsh

# Bundles from the default repository
antigen bundle git
antigen bundle zsh-users/zsh-autosuggestions
antigen bundle zsh-users/zsh-syntax-highlighting

# Load the theme.
antigen theme af-magic

# Tell Antigen that you're done.
antigen apply
```

> El tercer bloque de líneas, son los plugins que se desean añadir.

### 3. Cambiar shell

```bash
chsh -s `which zsh`
```

# Oh My ZSH

Es un framework desarrollado por la comunidad para gestionar la configuración de ZSH

## 1. Instalación:

```bash
wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | zsh
```

## 2. Visualizar las shells disponibles en nuestro sistema:

```bash
cat /etc/shells
```

## 3. Cambiar shell

Cambiar el shell a zsh:

```bash
chsh -s `which zsh`
```

Volver al shell por defecto:

```bash
chsh -s `which bash`
```

## 4. Conocer la shell actual:

```bash
echo $SHELL
```

## 5. Cambiar de tema

Se debe editar el archivo de configuración de zsh:

```bash
vim ~/.zshrc
```

Ahora se sustituye el nombre del tema actual por el que se desea, sustituyendo la línea `ZSH_THEME="<NombreDelTema>"`, por ejemplo:

```bash
ZSH_THEME="af-magic"
```

## 6. Pluggins

### 1. [zsh-autosuggestions:](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md)

Con base al historial, sugiere comandos a medida que se escribe. Para su instalación se debe seguir los siguientes pasos:

1. Clonar el repositorio dentro de `~/.oh-my-zsh/custom/plugins`:

    ```bash
    git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
    ```

2. Añadir el plugin a la lista de plugins para que se cargue (en del fichero ~ / .zshrc)

    ```
    plugins=(git zsh-autosuggestions)
    ```
    
3. Reinicie la terminal o ejecute: 

    ```
    source ~/.profile
    ```

# Temas

## 1. [Spaceship](https://github.com/denysdovhan/spaceship-prompt)

