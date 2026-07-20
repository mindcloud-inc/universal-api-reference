# Get Alias with Vercel

Retrieves an alias record from Vercel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/aliases/:idOrAlias`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Get Alias](https://docs.vercel.com/docs/rest-api/reference/endpoints/aliases/get-an-alias)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrAlias` | path | `string` | yes | The alias string or alias ID to retrieve. |
