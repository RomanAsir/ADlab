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
10.0.0.10                         DHCP dinamico
AD DS
DNS
DHCP

Dominio: empresa.local

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
UsuariosTopologia
DC01: Controlador de dominio, DNS y DHCP
PC01: Equipo cliente unido al dominio
Dominio: empresa.local
Red: Privada de laboratorio
Servicios configurados
Active Directory
Se instalo y configuro AD DS en el servidor DC01, promoviendo el equipo a controlador de dominio del bosque empresa.local.

DNS
El servicio DNS se integro con Active Directory para la resolucion de nombres internos dentro del dominio.

DHCP
Se configuro un ambito DHCP para asignar direcciones IP dinamicas a los equipos cliente de la red de laboratorio.

Usuarios, grupos y OU
Se creo una estructura organizativa por departamentos para simular una empresa real, incluyendo usuarios y grupos de seguridad.

GPO
Se aplicaron politicas de grupo para:

definir restricciones de seguridad,
controlar configuraciones de usuario,
mapear unidades de red,
personalizar el entorno del usuario.
Carpetas compartidas
Se configuraron recursos compartidos con permisos asignados mediante grupos, siguiendo buenas practicas de administracion.

Estructura organizativa
Empresa
|-- IT
|-- RRHH
|-- Finanzas
|-- Ventas
`-- Equipos
Usuarios creados
Ejemplo de usuarios del laboratorio:

juan.it
maria.rrhh
pedro.finanzas
laura.ventas
Grupos de seguridad
IT
RRHH
FINANZAS
VENTAS
Los permisos se asignaron a grupos en lugar de hacerlo directamente a usuarios, siguiendo el principio de minimo privilegio.

Pruebas realizadas
Durante el laboratorio se verifico el correcto funcionamiento de:

resolucion DNS con nslookup
conectividad con ping
asignacion de IP con ipconfig /all
pertenencia al dominio
aplicacion de politicas con gpupdate /force
diagnostico de dominio con whoami y gpresult
acceso a recursos compartidos
Comandos de diagnostico utilizados
ipconfig /all
ping 10.0.0.10
ping 10.0.0.1
hostname
nslookup empresa.local
whoami
whoami /groups
gpupdate /force
gpresult /r
net share
net use Z: \\dc01\IT
Troubleshooting
Se documentaron incidencias habituales como:

fallo en la union al dominio,
errores de DNS,
problemas de asignacion DHCP,
GPO no aplicada,
acceso denegado a carpetas compartidas.
Estas pruebas permiten demostrar capacidad de diagnostico y resolucion de problemas en un entorno Windows Server.

PowerShell
Se prepararon comandos y scripts basicos para la administracion del entorno, incluyendo automatizacion de tareas sobre Active Directory.

Ejemplo:

Import-Module ActiveDirectory

New-ADUser `
-Name "Juan Perez" `
-GivenName "Juan" `
-Surname "Perez" `
-SamAccountName "juan.perez" `
-UserPrincipalName "juan.perez@empresa.local" `
-Enabled $true `
-AccountPassword (ConvertTo-SecureString "Temporal123!" -AsPlainText -Force)
Conclusion
Este laboratorio reproduce una infraestructura empresarial basica y permite practicar tareas esenciales de administracion de sistemas Windows, como Active Directory, DNS, DHCP, GPO, usuarios, grupos, permisos y resolucion de incidencias.

Es un proyecto especialmente util como evidencia practica para un portfolio profesional orientado a entornos de sistemas y soporte tecnico.

Autor
Proyecto realizado como practica formativa de ASIR.
