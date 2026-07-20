# Create Lead with Notificações Inteligentes

Creates a new lead in Notificações Inteligentes.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads`
- **Base URL:** `https://api.notificacoesinteligentes.com`
- **Official documentation:** [Create Lead](https://docs.notificacoesinteligentes.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Lead email address. |
| `name` | body | `string` | yes | Lead name. |
| `phone` | body | `string` | yes | Lead phone number with country code. |
