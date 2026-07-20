# List AFIR Charge Points with Monta

Retrieves AFIR-compliant charge points from Monta.

## Endpoint

- **Method:** `GET`
- **Path:** `/afir/charge-points`
- **Base URL:** `https://public-api.monta.com/api/v1`
- **Official documentation:** [List AFIR Charge Points](https://docs.public-api.monta.com/reference/get-afir-charge-points)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `list<string>` | yes | ISO 3166-1 alpha-2 country code. Supported values are DK and BE. Accepted values: `BE`, `DK`. |
| `page` | query | `number` | no | AFIR page number to retrieve. This endpoint starts at page 1. |
| `perPage` | query | `number` | no | Number of AFIR results per page, up to 1000. |
