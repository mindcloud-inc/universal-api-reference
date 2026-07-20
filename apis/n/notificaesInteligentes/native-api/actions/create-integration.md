# Create Integration with Notificações Inteligentes

Creates a new integration in Notificações Inteligentes.

## Endpoint

- **Method:** `POST`
- **Path:** `/integrations`
- **Base URL:** `https://api.notificacoesinteligentes.com`
- **Official documentation:** [Create Integration](https://docs.notificacoesinteligentes.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Integration name. |
| `platform` | body | `string` | yes | Integration platform slug. |
