# Create Tag with Notificações Inteligentes

Creates a new tag in Notificações Inteligentes.

## Endpoint

- **Method:** `POST`
- **Path:** `/tags`
- **Base URL:** `https://api.notificacoesinteligentes.com`
- **Official documentation:** [Create Tag](https://docs.notificacoesinteligentes.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `color` | body | `string` | no | Tag color in hexadecimal. |
| `description` | body | `string` | no | Tag description. |
| `label` | body | `string` | yes | Tag label. |
