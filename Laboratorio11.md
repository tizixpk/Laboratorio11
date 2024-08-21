# Tiziano Pirez 4to 4ta 
# Comandos DiskPart
## 1. Listado de Discos Disponibles:
```bash
list disk
```
- Muestra todos los discos disponibles en el sistema.

## 2. Selección de Disco:
```bash
select disk 1
```
- Selecciona el disco 1 para realizar operaciones.

## 3. Creación de Partición Primaria:
```bash
create partition primary
```
- Crea una partición primaria en el disco seleccionado.

## 4. Formateo de la Partición:
```bash
format fs=ntfs label="DATOS"
```
- Formatea la partición con el sistema de archivos NTFS y le asigna la etiqueta "DATOS".

## 5. Activación y Asignación de Letra:
```bash
active
assign letter=Z
```
- Activa la partición y le asigna la letra "Z".

## 6. Redimensionamiento de Partición:
```bash
shrink desired=1500
```
- Redimensiona la partición "DATOS" reduciéndola en 1500MB.

## 7. Creación de Nuevas Particiones:
```bash
create partition primary size=500
```
- Crea una nueva partición primaria de 500MB. Repetir este comando tres veces para crear tres particiones.

## 8. Formateo y Asignación de Letra a la Nueva Partición:
```bash
select partition 2
format fs=fat32 label="Imagenes"
assign letter=Y
```
- Selecciona la segunda partición, la formatea como FAT32 con la etiqueta "Imágenes" y le asigna la letra "Y".

**9. Comprobación de Particiones:**
```bash
list partition
```
- Lista todas las particiones en el disco para verificar su estado.

### Resultado Final
Se han creado y formateado varias particiones en un disco virtual, con las etiquetas "Documentos", "Imágenes", "Videos", y "Música", y se les han asignado letras específicas para su acceso.
