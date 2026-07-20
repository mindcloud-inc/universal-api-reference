# Update Page with Big Cartel

Updates an existing page in Big Cartel.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/accounts/[:account-id]/pages/[:page-id]`
- **Base URL:** `https://api.bigcartel.com`
- **Official documentation:** [Update Page](https://developers.bigcartel.com/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `number` | yes | The Big Cartel account ID. |
| `page-id` | path | `string` | yes | The Big Cartel page ID. |
| `data.id` | body | `string` | yes | — |
| `data.attributes.name` | body | `string` | yes | — |
| `data.attributes.content` | body | `string` | no | — |
| `data.attributes.use_layout` | body | `boolean` | no | — |
