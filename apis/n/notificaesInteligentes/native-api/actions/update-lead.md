# Update Lead with Notificações Inteligentes

Updates an existing lead in Notificações Inteligentes.

## Endpoint

- **Method:** `PUT`
- **Path:** `/leads/:lead`
- **Base URL:** `https://api.notificacoesinteligentes.com`
- **Official documentation:** [Update Lead](https://docs.notificacoesinteligentes.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Lead email address. |
| `lead` | path | `string` | yes | The lead identifier. |
| `name` | body | `string` | no | Lead name. |
