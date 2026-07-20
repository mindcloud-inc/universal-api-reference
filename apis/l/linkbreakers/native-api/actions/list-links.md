# List Links with Linkbreakers

Retrieves a list of links from Linkbreakers.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/links`
- **Base URL:** `https://api.linkbreakers.com`
- **Official documentation:** [List Links](https://linkbreakers.com/help/api/links#list-links)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Filter links by name or shortlink search. |
| `tags[]` | query | `array<string>` | no | Filter links by tags; matches links containing any provided tag. |
| `directoryId` | query | `string` | no | Filter links by one directory ID. |
| `includeAllDirectories` | query | `boolean` | no | Ignore the directory filter and return links from all directories. |
| `sortBy` | query | `string` | no | Field used to sort links. |
| `sortDirection` | query | `string` | no | Sort direction for list ordering. |
| `include[]` | query | `array<string>` | no | Related link resources to include in the response. |
