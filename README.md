Proyecto Active Directory con Windows Server 2022
Descripción
Laboratorio práctico realizado como parte de la formación en ASIR con el objetivo de simular la infraestructura básica de una pequeña empresa mediante una red virtual aislada.

El entorno ha sido desplegado utilizando VMware Workstation y está compuesto por un controlador de dominio con Windows Server 2022 y un equipo cliente con Windows 11, sobre los que se han implementado servicios y tareas habituales de administración de sistemas.

Este proyecto está basado en un entorno de laboratorio con direcciones IP privadas, nombres ficticios y una empresa inventada con fines educativos.

Objetivos del proyecto
Desplegar un dominio Active Directory.
Configurar un controlador de dominio.
Integrar DNS con Active Directory.
Implementar DHCP para asignación dinámica de direcciones IP.
Crear y administrar usuarios y grupos.
Diseñar una estructura organizativa mediante unidades organizativas (OU).
Aplicar directivas de grupo (GPO).
Unir equipos Windows al dominio.
Configurar carpetas compartidas y permisos.
Documentar incidencias y tareas de troubleshooting.
Tecnologías utilizadas
VMware Workstation
Windows Server 2022 Standard Evaluation
Windows 11 Pro
Active Directory Domain Services (AD DS)
DNS Server
DHCP Server
Group Policy Objects (GPO)
PowerShell
Arquitectura del laboratorio
```text
VMware NAT
10.0.0.1
|
-----------------------------------
| |
DC01 PC01
Windows Server 2022 Windows 11 Pro
10.0.0.10 DHCP dinámico
AD DS
DNS
DHCP

Dominio: empresa.local
```

Capturas del laboratorio
1. Concesiones de direcciones
Concesiones de direcciones

2. DHCP
DHCP

3. Directiva de grupo
Directiva GPO

4. DNS
DNS

5. Dominio
Dominio

6. Estructura de Active Directory
Estructura AD

7. Grupos
Grupos

8. Miembros de grupo
Miembros de grupo

9. Ping
Ping

10. Usuario
Usuario

11. Usuarios
Usuarios

Topología
DC01: Controlador de dominio, DNS y DHCP
PC01: Equipo cliente unido al dominio
Dominio: empresa.local
Red: Privada de laboratorio
Servicios configurados
Active Directory
Se instaló y configuró AD DS en el servidor DC01, promoviendo el equipo a controlador de dominio del bosque empresa.local.

DNS
El servicio DNS se integró con Active Directory para la resolución de nombres internos dentro del dominio.

DHCP
Se configuró un ámbito DHCP para asignar direcciones IP dinámicas a los equipos cliente de la red de laboratorio.

Usuarios, grupos y OU
Se creó una estructura organizativa por departamentos para simular una empresa real, incluyendo usuarios y grupos de seguridad.

GPO
Se aplicaron políticas de grupo para:

definir restricciones de seguridad,
controlar configuraciones de usuario,
mapear unidades de red,
personalizar el entorno del usuario.
Carpetas compartidas
Se configuraron recursos compartidos con permisos asignados mediante grupos, siguiendo buenas prácticas de administración.

Estructura organizativa
Empresa
IT
RRHH
Finanzas
Ventas
Equipos
Usuarios creados
juan.it
maria.rrhh
pedro.finanzas
laura.ventas
Grupos de seguridad
IT
RRHH
FINANZAS
VENTAS
Los permisos se asignaron a grupos en lugar de hacerlo directamente a usuarios, siguiendo el principio de mínimo privilegio.

Pruebas realizadas
Resolución DNS con nslookup
Conectividad con ping
Asignación de IP con ipconfig /all
Pertenencia al dominio
Aplicación de políticas con gpupdate /force
Diagnóstico de dominio con whoami y gpresult
Acceso a recursos compartidos
Troubleshooting
Fallo en la unión al dominio
Errores de DNS
Problemas de asignación DHCP
GPO no aplicada
Acceso denegado a carpetas compartidas
Conclusión
Este laboratorio reproduce una infraestructura empresarial básica y permite practicar tareas esenciales de administración de sistemas Windows, como Active Directory, DNS, DHCP, GPO, usuarios, grupos, permisos y resolución de incidencias.


