# Crear una USB booteable

## 1. Identificar el punto de montaje del dispositivo

```bash
sudo fdisk -l
```

## 2. Formatear la USB

### 2.1 Desmontar el dispositivo:

```bash
umount /dev/sd<?> 
```

### 2.2 Formatear USB en FAT32

```bash
mkfs.vfat -F 32 /dev/sd<?>  -I
```

## 3 Comando dd

Se indica al comando dd el punto de montahe de nuestra USB, así como la ruta de la imagen del disco que sera copiado.

```bash
sudo dd if=<imagenDisco> of=/dev/sd<?> bs=512k status=progress conv=fdatasync
```

+ `bs:` Lee y escribe N bytes
+ `conv=fdatasyncbit`: es importante, ya que dd puede retornar antes de que finalice la operación de escritura.
+ `status=progress`: Muestra el progreso.