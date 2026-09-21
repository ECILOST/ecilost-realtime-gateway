# ECILOST Realtime Gateway

Esqueleto para distribuir eventos de sala desde RabbitMQ. No contiene reglas de puja ni estado de negocio autoritativo.

```text
src/
  auth/ connections/ broker/ snapshots/ presentation/ws/ common/
test/
```

WebSocket o SSE sigue pendiente de decisión; no se crean endpoints aún.

Los mensajes se consumen de forma independiente e idempotente. El Gateway no es serializador de pujas ni coordinador transaccional: conserva el orden publicado por cada `roomId` y puede escalar horizontalmente para salas diferentes.
