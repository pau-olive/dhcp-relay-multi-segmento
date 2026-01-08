# Servidor DHCP en Linux y Windows con Relay

![Portada del proyecto](cover.png)

## Descripción del Proyecto
Proyecto personal de **Administración de Sistemas** enfocado en la configuración de un servidor DHCP en Linux (isc-dhcp-server) y Windows, con relay para asignar IPs en múltiples segmentos de red.

Características principales:
- Pools de IPs en dhcpd.conf para segmentos 172.10.0.0/24 y 172.10.2.0/24.
- Configuración de interfaces en netplan.
- isc-dhcp-relay para reenviar peticiones DHCP.
- Verificación con clientes: ipconfig /all y mtr google.es.
- DHCP en Windows: rol DHCP, scopes, enrutamiento y NAT.
- Rutas estáticas para conectividad entre segmentos.
- Configuración de relay en Windows.
- Pruebas de asignación IP, gateway, DNS e internet en clientes.

Entorno reproducible en Linux/Windows con relay para redes segmentadas.

## Tecnologías y Herramientas Utilizadas
- **isc-dhcp-server** para DHCP en Linux
- **isc-dhcp-relay** para relay en Linux
- **Windows Server DHCP** para rol y scopes
- Netplan para interfaces de red
- Comandos: ipconfig /all, mtr, systemctl status
- Enrutamiento, NAT y rutas estáticas para conectividad

## Objetivos Alcanzados
- Asignación automática de IPs en múltiples segmentos.
- Reenvío de peticiones DHCP con relay.
- Configuración de scopes, NAT y rutas estáticas en Windows.
- Verificación de conectividad e internet en clientes.
- Enrutamiento correcto entre segmentos.

## Proceso Completo – Explicación Detallada

### 1. Configuración DHCP en Linux (dhcpd.conf)
Definición de pools para segmentos con range, routers y domain-name-servers.

### 2. Interfaces de Red en Netplan (servidor DHCP)
Configuración de IPs estáticas en interfaces del servidor DHCP.

### 3. Configuración isc-dhcp-relay
SERVERS con IP del DHCP central e INTERFACES para reenviar peticiones.

### 4. Interfaces de Red en Netplan (servidor relay)
Configuración de IPs en interfaces del relay.

### 5. Verificación en Cliente 172.10.0.0/24 (Linux DHCP)
ipconfig /all para IP, gateway, DNS; mtr google.es para internet.

### 6. Verificación en Cliente 172.10.2.0/24 (Linux DHCP)
Lo mismo para el otro segmento, confirmando relay.

### 7. Configuración DHCP en Windows (rol DHCP)
Instalación rol, scopes para segmentos, opciones (routers, DNS).

### 8. Configuración NAT y Enrutamiento en Windows
Routing and Remote Access con NAT para salida a internet.

### 9. Ruta Estática en Windows para 172.10.2.0/24
Ruta a través del relay (172.10.1.2).

### 10. Configuración Relay en Windows
Agent retransmissor DHCP y enrutamiento.

### 11. Verificación en Cliente 172.10.0.0/24 (Windows DHCP)
ipconfig /all y mtr google.es.

### 12. Verificación en Cliente 172.10.2.0/24 (Windows DHCP)
Lo mismo para el otro segmento.

## Capturas del Proceso Completo

<div style="display: grid; grid-template-columns: repeat(auto-fill, minmax(320px, 1fr)); gap: 15px; margin: 30px 0;">

  <img src="screenshots/screenshots (1).png" alt="Paso 1">
  <img src="screenshots/screenshots (2).png" alt="Paso 2">
  <img src="screenshots/screenshots (3).png" alt="Paso 3">
  <img src="screenshots/screenshots (4).png" alt="Paso 4">
  <img src="screenshots/screenshots (5).png" alt="Paso 5">
  <img src="screenshots/screenshots (6).png" alt="Paso 6">
  <img src="screenshots/screenshots (7).png" alt="Paso 7">
  <img src="screenshots/screenshots (8).png" alt="Paso 8">
  <img src="screenshots/screenshots (9).png" alt="Paso 9">
  <img src="screenshots/screenshots (10).png" alt="Paso 10">
  <img src="screenshots/screenshots (11).png" alt="Paso 11">
  <img src="screenshots/screenshots (12).png" alt="Paso 12">
  <img src="screenshots/screenshots (13).png" alt="Paso 13">
  <img src="screenshots/screenshots (14).png" alt="Paso 14">
  <img src="screenshots/screenshots (15).png" alt="Paso 15">
  <img src="screenshots/screenshots (16).png" alt="Paso 16">
  <img src="screenshots/screenshots (17).png" alt="Paso 17">
  <img src="screenshots/screenshots (18).png" alt="Paso 18">
  <img src="screenshots/screenshots (19).png" alt="Paso 19">
  <img src="screenshots/screenshots (20).png" alt="Paso 20">

</div>

> Las 20 capturas muestran el flujo completo: configs en Linux/Windows, relay, rutas, NAT y pruebas en clientes.

## Aprendizajes Clave
- **DHCP Linux**: Pools, relay y netplan para multi-segmento.
- **DHCP Windows**: Rol, scopes, NAT y routing.
- **Relay**: Reenvío de peticiones entre segmentos.
- Verificaciones: ipconfig y mtr para IP y conectividad.

## Relevancia Professional
Habilidades para:
- Redes empresariales (DHCP multi-segmento).
- Admin de servidores (Linux/Windows hybrid).
- Cloud/DevOps (base para DHCP en AWS VPC, Azure).

## Conclusión
Proyecto funcional con DHCP y relay en Linux/Windows, listo para redes reales.

¡Gracias por visitar! Dale ⭐ si te gusta.

---
**Autor**: Pau Olivé Moreno  
**Fecha**: Principios de 2025