# Update Tag with Notificações Inteligentes

Updates an existing tag in Notificações Inteligentes.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tags/:tag`
- **Base URL:** `https://api.notificacoesinteligentes.com`
- **Official documentation:** [Update Tag](https://docs.notificacoesinteligentes.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `color` | body | `string` | no | Tag color in hexadecimal. |
| `description` | body | `string` | no | Tag description. |
| `label` | body | `string` | no | Tag label. |
| `tag` | path | `string` | yes | The tag identifier. |
