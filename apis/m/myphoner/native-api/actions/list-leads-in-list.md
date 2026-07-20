# List Leads in List with Myphoner

Retrieves leads from a list in Myphoner.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:listId/leads`
- **Base URL:** `https://{subdomain}.myphoner.com/api/v2`
- **Official documentation:** [List Leads in List](https://www.myphoner.com/docs/api/#lists)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `number` | yes | The Myphoner list ID. |
| `order` | query | `string` | no | Use last_updated_first to return the most recently updated leads first. |
