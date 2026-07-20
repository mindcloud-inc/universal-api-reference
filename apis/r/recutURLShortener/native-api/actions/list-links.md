# List Links with Recut URL Shortener

Retrieves links from Recut URL Shortener.

## Endpoint

- **Method:** `GET`
- **Path:** `/urls`
- **Base URL:** `https://app.recut.in/api`
- **Official documentation:** [List Links](https://app.recut.in/developers#list-links)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order` | query | `string` | no | Sort links by `date` or `click`. |
| `short` | query | `string` | no | Search using the short URL. When provided, the docs say other parameters are ignored. |
| `q` | query | `string` | no | Search links using a keyword. |
