# Ejercicio 7 - Modelo Entidad-Relación de un Sistema de Gestión Hotelera

## Descripción
Este ejercicio consiste en diseñar un modelo Entidad-Relación (DER) para un sistema de gestión de hoteles. El modelo permite administrar hoteles, habitaciones, huéspedes, reservas y consumos/servicios, representando las relaciones operativas entre la infraestructura del hotel, los clientes y sus estancias.

## Entidades y atributos

### 1. Hotel
Representa los establecimientos hoteleros disponibles en la cadena o red.
- **id_hotel**: identificador único del hotel.
- **nombre**: nombre del hotel.
- **direccion**: dirección física del establecimiento.
- **telefono**: número de contacto del hotel.
- **calificacion**: categoría o calificación del hotel.

### 2. Habitación
Representa las unidades de alojamiento dentro de un hotel.
- **nro_habitacion**: número o identificador de la habitación.
- **id_hotel**: identificador del hotel al que pertenece.
- **numero**: número de la habitación.
- **piso**: nivel o piso en el que se ubica.
- **estado**: disponibilidad o estado actual de la habitación.
- **tipo**: categoría o tipo de habitación (ej. simple, doble, suite).
- **precio**: tarifa por noche.

### 3. Huésped
Representa a los clientes que se hospedan o realizan reservas en el hotel.
- **id_huesped**: identificador único del huésped.
- **nombre**: nombre del huésped.
- **apellido**: apellido del huésped.
- **dni**: documento de identidad.
- **telefono**: número de contacto.
- **correo**: correo electrónico.

### 4. Reserva
Representa las solicitudes o registros de estancia realizados por los huéspedes.
- **id_reserva**: identificador único de la reserva.
- **id_hotel**: identificador del hotel asociado.
- **estado**: estado de la reserva (ej. confirmada, cancelada, pendiente).
- **inicio**: fecha de inicio de la reserva.
- **fin**: fecha de finalización de la reserva.
- **codigo**: código alfanumérico de confirmación.

### 5. Consumo/Servicio
Representa los consumos extras o servicios adicionales utilizados durante la estancia.
- **id_consumo**: identificador único del consumo.
- **id_habitacion**: identificador de la habitación asociada.
- **cantidad**: unidades consumidas del servicio.
- **tipo servicio**: descripción o categoría del servicio (ej. minibar, lavandería, restaurante).
- **costo**: precio o valor del consumo.

## Relaciones y cardinalidades
- **Hotel – Habitación (Tiene / 1:N)**: un hotel cuenta con múltiples habitaciones, mientras que cada habitación pertenece a un único hotel.
- **Hotel – Reserva (Necesita / 1:N)**: un hotel gestiona y registra varias reservas asociadas a sus instalaciones.
- **Huésped – Reserva (Realiza / 1:N)**: un huésped puede realizar una o más reservas, y cada reserva está vinculada a un huésped específico.
- **Reserva – Habitación (Ocupa / 1:N)**: una reserva asigna una o varias habitaciones para la estancia del huésped.
- **Habitación – Consumo/Servicio (Incluye / 1:N)**: una habitación puede registrar diversos consumos o servicios adicionales durante la estancia.

## Objetivo
Diseñar una base de datos que permita organizar de manera integral la información de un sistema de gestión hotelera, facilitando el control de establecimientos, habitaciones, registro y seguimiento de huéspedes, administración de reservas y el cobro de servicios o consumos adicionales.
