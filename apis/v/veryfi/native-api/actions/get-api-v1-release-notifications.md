# Get release notifications with Veryfi

Retrieves release notifications from Veryfi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/release-notifications`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Get release notifications](https://docs.veryfi.com/api/get-release-notifications/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Default value: 1 |
| `page_size` | query | `number` | no | Default value: 50 |
| `product` | query | `string` | no | — |
| `environment` | query | `string` | no | Default value: production |
