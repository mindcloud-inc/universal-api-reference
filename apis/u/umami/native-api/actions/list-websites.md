# List Websites with Umami

## Endpoint

- **Method:** `GET`
- **Path:** `/websites`
- **Base URL:** `https://api.umami.is/v1`
- **Official documentation:** [List Websites](https://docs.umami.is/docs/api/websites)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeTeams` | query | `boolean` | no | Include websites where you are the team owner. |
| `search` | query | `string` | no | Search text used to filter websites. |
