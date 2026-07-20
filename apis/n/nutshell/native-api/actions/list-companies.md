# List Companies with Nutshell

Retrieves companies from Nutshell.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts`
- **Base URL:** `https://app.nutshell.com/rest`
- **Official documentation:** [List Companies](https://developers.nutshell.com/reference)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search across companies. |
| `email` | query | `string` | no | Filter companies by contact email address. |
