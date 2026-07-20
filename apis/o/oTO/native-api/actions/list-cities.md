# List Cities with OTO

Retrieves cities from the OTO API.

## Endpoint

- **Method:** `POST`
- **Path:** `/getCities`
- **Base URL:** `https://api.tryoto.com/rest/v2`
- **Official documentation:** [List Cities](https://help.tryoto.com/en/support/solutions/articles/150000213813-carrier-integrations-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | body | `string` | yes | Two-letter country code to list cities for. |
| `perPage` | body | `number` | no | Maximum number of cities to return per page. |
| `page` | body | `number` | no | Page number to fetch. |
