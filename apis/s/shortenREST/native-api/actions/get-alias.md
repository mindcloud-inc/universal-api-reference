# Get Alias with Shorten.REST

Retrieves alias details from Shorten.REST by alias and domain.

## Endpoint

- **Method:** `GET`
- **Path:** `/aliases`
- **Base URL:** `https://api.shorten.rest`
- **Official documentation:** [Get Alias](https://docs.shorten.rest/#GET--aliases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domainName` | query | `string` | no | The domain which the alias belongs to, without http/https or trailing slash. |
| `aliasName` | query | `string` | yes | The alias value without a leading slash. |
