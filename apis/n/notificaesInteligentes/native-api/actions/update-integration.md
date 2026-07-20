# Update Integration with Notificações Inteligentes

Updates an existing integration in Notificações Inteligentes.

## Endpoint

- **Method:** `PUT`
- **Path:** `/integrations/:store`
- **Base URL:** `https://api.notificacoesinteligentes.com`
- **Official documentation:** [Update Integration](https://docs.notificacoesinteligentes.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Integration name. |
| `store` | path | `string` | yes | The integration store identifier. |
