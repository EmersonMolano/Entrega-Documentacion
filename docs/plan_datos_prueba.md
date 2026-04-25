# Plan de Poblamiento de Datos de Prueba

## Orden de inserción (según dependencias de claves foráneas)

1. Geografía y Datos de Referencia (time_zone, continent, country, etc.)
2. Aerolínea
3. Identidad (person_type, person, etc.)
4. Seguridad (user_status, security_role, etc.)
5. Clientes y Fidelización
6. Aeropuerto
7. Aeronaves
8. Operaciones de Vuelo
9. Ventas, Reservas y Tiquetes
10. Abordaje
11. Pagos
12. Facturación

## Estructura de scripts recomendada
- `scripts/data/01-geography-reference.sql`
- `scripts/data/02-airline.sql`
- `scripts/data/03-identity.sql`
- `scripts/data/12-billing.sql`

Cada script incluirá:
- INSERT con datos realistas.
- Comentarios explicando la dependencia.
- Validaciones finales (SELECT COUNT(*) FROM tabla;)

Este orden garantizaria que no fallen las restricciones de integridad referencial en el script.