
<div align="center">

# TP Integrador - Computación Aplicada
### Universidad de Palermo

![Debian](https://img.shields.io/badge/Debian-12-blue?style=for-the-badge&logo=debian)
![Apache](https://img.shields.io/badge/Apache-D22128?style=for-the-badge&logo=apache)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnu-bash)

Proyecto de administración de sistemas Linux sobre máquina virtual Debian 12.

[Descripción](#descripción) • [Características](#características) • [Equipo](#equipo-de-desarrollo) • [Script de Backup](#script-de-backup)

</div>


---

## 📝 Descripción

Este trabajo práctico integrador consiste en la puesta en producción de un servidor seguro y automatizado. Se configuró una máquina virtual con Debian 12 (Bookworm), implementando servicios web, base de datos, gestión de almacenamiento y tareas programadas de respaldo.

## ⚙️ Características

### 🌐 Red y Seguridad
*   **Configuración de Red:** IP estática en modo Puente (Bridge) dentro del rango de la LAN física.
*   **Acceso Remoto:** Servicio SSH configurado para acceso root mediante autenticación de clave pública/privada.

### 💻 Servicios
*   **Web Server:** Instalación de Apache2 con soporte para PHP.
*   **Base de Datos:** Motor MariaDB con carga de script SQL inicial.
*   **Contenido:** Servidor configurado para servir archivos desde `/www_dir`.

### 💾 Almacenamiento
*   **Particionado:** Agregado de disco de 10GB particionado manualmente.
*   **Montajes:** Configuración de `/www_dir` y `/backup_dir` con montaje automático vía `fstab`.
*   **Persistencia:** Registro de particiones en `/opt/particion`.

### ⏰ Automatización (Backup)
*   **Scripting:** Desarrollo de script `backup_full.sh` con validaciones y formato de fecha.
*   **Programación:** Tareas automatizadas mediante Cron para respaldos diarios y alternos.

---

## 🛠️ Script de Backup

El script instalado en `/opt/scripts/backup_full.sh` permite generar copias de seguridad comprimidas.

**Uso:**
```bash
./backup_full.sh <directorio_origen> <directorio_destino>
```

**Ejemplo:**
```bash
/opt/scripts/backup_full.sh /var/log /backup_dir
```

**Opciones:**
*   `-help`: Muestra la ayuda y guía de uso.

---

## 👥 Equipo de Desarrollo

| Integrante |
| :--- |
| **Agustina Esposito** |
| **Jose Alvarez** |
| **Lautaro Pintos** |

---

<div align="center">
© 2026 - Universidad de Palermo
</div>
