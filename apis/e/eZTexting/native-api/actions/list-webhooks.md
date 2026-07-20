# List Webhooks with EZ Texting

Retrieves webhooks from EZ Texting.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhooks/subscriptions`
- **Base URL:** `https://a.eztexting.com/v1`
- **Official documentation:** [List Webhooks](https://developers.eztexting.com/reference/list_8-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page offset starting at 0 |
| `size` | query | `number` | no | Page size |
| `sort` | query | `string` | no | Sort field and direction |
