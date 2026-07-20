# Delete Alias with Shorten.REST

Deletes an existing alias from Shorten.REST.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/aliases`
- **Base URL:** `https://api.shorten.rest`
- **Official documentation:** [Delete Alias](https://docs.shorten.rest/#DELETE--aliases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domainName` | query | `string` | no | The domain which the alias belongs to, without http/https or trailing slash. |
| `aliasName` | query | `string` | yes | The alias value without a leading slash. |
