# List CRM Tickets with ChatDaddy

Retrieves CRM ticket records from ChatDaddy.

## Endpoint

- **Method:** `GET`
- **Path:** `/crm/tickets`
- **Base URL:** `https://api.chatdaddy.tech/im`
- **Official documentation:** [List CRM Tickets](https://chatdaddy.stoplight.io/docs/openapi/513fed376d8bc-get-crm-tickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `number` | no | Number of CRM tickets to return. |
| `nextPageCursor` | query | `string` | no | Cursor for the next CRM ticket page. |
