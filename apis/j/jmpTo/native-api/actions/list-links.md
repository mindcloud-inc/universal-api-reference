# List Links with JmpTo

Retrieves links from JmpTo.

## Endpoint

- **Method:** `GET`
- **Path:** `/urls`
- **Base URL:** `https://jmpto.net/api`
- **Official documentation:** [List Links](https://jmpto.net/developers#list-links)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order` | query | `string` | no | Sort order for returned links. JmpTo's example uses date. |
| `q` | query | `string` | no | Search links using a keyword. |
| `short` | query | `string` | no | Search using the short URL. When this is used, other parameters are ignored and a single-link response may be returned. |
