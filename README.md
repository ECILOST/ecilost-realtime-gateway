# ECILOST Realtime Gateway

Proyecto base de NestJS para un futuro gateway de eventos de sala. El código actual inicia el proceso y carga configuración. El protocolo de transporte, la autenticación y el consumo de RabbitMQ están pendientes de implementación.

## Inicio local

```bash
cp .env.example .env
npm install
npm run start:dev
```

El proceso escucha en `PORT`, con valor local por defecto `3004`. El canal Socket.IO operativo vive en Engagement, en el puerto `3005` y el namespace `/realtime`. Su README documenta el JWT del handshake, las suscripciones y la reconexión. Este repositorio aún carece de rutas HTTP para publicar OpenAPI.

## Estructura y comprobación

- [Autenticación de conexiones prevista](src/auth/README.md)
- [Integración prevista con RabbitMQ](src/broker/README.md)

```bash
npm run typecheck
npm run build
```
