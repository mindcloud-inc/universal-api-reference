# List Subscribers with SimpleCirc

Retrieves a list of subscribers from SimpleCirc.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1.2/subscribers`
- **Base URL:** `https://simplecirc.com`
- **Official documentation:** [List Subscribers](https://simplecirc.com/docs/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `limit` | query | `number` | no |
| `email` | query | `string` | no |
| `starting_after` | query | `string` | no |
