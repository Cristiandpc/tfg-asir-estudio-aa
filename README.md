# Proyecto Final ASIR – Infraestructura para un estudio de videojuegos (AA)

**Diseño y Despliegue de la Infraestructura de Red, Almacenamiento y Servicios Centralizados para un Estudio de Desarrollo de Videojuegos.**

Integrantes: Cristian De Paz Comendador · Álex Martínez Vallejo
Curso 2026/2027 – 2º ASIR

Este repositorio contiene la parte práctica del proyecto: configuraciones, scripts, ficheros de despliegue y capturas de las pruebas. La memoria se redacta aparte (Google Drive).

## Estructura

| Carpeta | Contenido | Parte |
|---|---|---|
| `01-Red/` | Exportación de la configuración de pfSense (sin secretos) y esquema de red | A |
| `02-VPN/` | Configuración de WireGuard (sin claves privadas) | A |
| `03-Servicios/` | `docker-compose.yml` de Nextcloud y Jellyfin, `smb.conf`, `exports` | B |
| `04-Backups/` | Scripts de copia y restauración, crontab, logs de ejemplo | A |
| `05-Pruebas/` | Capturas de cada prueba del RFTP (nombre: `R02F01T02P01.png`) | A y B |
| `06-Video-demo/` | Enlace al vídeo de demostración | A y B |

## Datos de la infraestructura

| VLAN | Uso | Red |
|---|---|---|
| 10 | Desarrollo y Arte | 10.10.10.0/24 |
| 20 | QA y Marketing | 10.10.20.0/24 |
| 30 | Dirección | 10.10.30.0/24 |
| 99 | Servidores | 10.10.99.0/24 |
| VPN | WireGuard | 10.10.200.0/24 |

srv-servicios: 10.10.99.10 · srv-backup: 10.10.99.20 · Dominio interno: `estudio.local`

## Normas del repositorio

1. Antes de empezar a trabajar: **Fetch / Pull**. Al terminar: **Commit + Push**.
2. Cada uno trabaja en las carpetas de su parte.
3. Mensajes de commit: `[A] R02: reglas del cortafuegos para la VLAN 20`.
4. **Nunca** se suben contraseñas, claves privadas ni ficheros `.env` reales (se usa `.env.example`).
5. Nada de máquinas virtuales, ISOs ni vídeos: solo enlaces.
