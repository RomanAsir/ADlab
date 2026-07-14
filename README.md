# Proyecto Active Directory con Windows Server 2022

## Descripción

Laboratorio práctico realizado como parte de la formación en ASIR con el objetivo de simular la infraestructura básica de una pequeña empresa mediante una red virtual aislada.

El entorno ha sido desplegado utilizando VMware Workstation y está compuesto por un controlador de dominio con Windows Server 2022 y un equipo cliente con Windows 11, sobre los que se han implementado servicios y tareas habituales de administración de sistemas.

> Este proyecto está basado en un entorno de laboratorio con direcciones IP privadas, nombres ficticios y una empresa inventada con fines educativos.

---

## Objetivos del proyecto

- Desplegar un dominio Active Directory.
- Configurar un controlador de dominio.
- Integrar DNS con Active Directory.
- Implementar DHCP para asignación dinámica de direcciones IP.
- Crear y administrar usuarios y grupos.
- Diseñar una estructura organizativa mediante unidades organizativas (OU).
- Aplicar directivas de grupo (GPO).
- Unir equipos Windows al dominio.
- Configurar carpetas compartidas y permisos.
- Documentar incidencias y tareas de troubleshooting.

---

## Tecnologías utilizadas

- VMware Workstation
- Windows Server 2022 Standard Evaluation
- Windows 11 Pro
- Active Directory Domain Services (AD DS)
- DNS Server
- DHCP Server
- Group Policy Objects (GPO)
- PowerShell

---

## Arquitectura del laboratorio

```text
                 VMware NAT
                10.0.0.1
                      |
        -----------------------------------
        |                                 |
     DC01                              PC01
Windows Server 2022               Windows 11 Pro
10.0.0.10                         DHCP dinámico
AD DS
DNS
DHCP

Dominio: empresa.local

## Capturas del laboratorio

### 1. Concesiones de direcciones
![Concesiones de direcciones](imagenes/01-concesiones-direcciones.png)

### 2. DHCP
![DHCP](imagenes/02-dhcp.png)

### 3. Directiva de grupo
![Directiva GPO](imagenes/03-directiva-gpo.png)

### 4. DNS
![DNS](imagenes/04-dns.png)

### 5. Dominio
![Dominio](imagenes/05-dominio.png)

### 6. Estructura de Active Directory
![Estructura AD](imagenes/06-estructura-ad.png)

### 7. Grupos
![Grupos](imagenes/07-grupos.png)

### 8. Miembros de grupo
![Miembros de grupo](imagenes/08-miembros-grupo.png)

### 9. Ping
![Ping](imagenes/09-ping.png)

### 10. Usuario
![Usuario](imagenes/10-usuario.png)

### 11. Usuarios
![Usuarios](imagenes/11-usuarios.png)

