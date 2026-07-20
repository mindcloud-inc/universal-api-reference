# List Designs with Canva

Retrieves designs from the current Canva user's projects.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/designs`
- **Base URL:** `https://api.canva.com/rest`
- **Official documentation:** [List Designs](https://www.canva.dev/docs/connect/api-reference/designs/list-designs/)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Search term used to filter the user's designs. Maximum length: 255. |
| `ownership` | query | `list` | no | Filter designs by whether they are owned by or shared with the user. Accepted values: `any`, `owned`, `shared`. |
| `continuation` | query | `string` | no | Continuation token returned by a previous List Designs call. |
