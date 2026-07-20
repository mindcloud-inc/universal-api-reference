# Create Page with Big Cartel

Creates a page in Big Cartel.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/[:account-id]/pages`
- **Base URL:** `https://api.bigcartel.com`
- **Official documentation:** [Create Page](https://developers.bigcartel.com/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `number` | yes | The Big Cartel account ID. |
| `data.attributes.name` | body | `string` | yes | — |
| `data.attributes.content` | body | `string` | no | — |
| `data.attributes.use_layout` | body | `boolean` | no | — |
