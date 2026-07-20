# List Aliases by Domain with Shorten.REST

Retrieves aliases from Shorten.REST for a specific domain.

## Endpoint

- **Method:** `GET`
- **Path:** `/aliases/all`
- **Base URL:** `https://api.shorten.rest`
- **Official documentation:** [List Aliases by Domain](https://docs.shorten.rest/#GET--aliases-all)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domainName` | query | `string` | no | The domain name to get aliases for, without http/https or trailing slash. |
