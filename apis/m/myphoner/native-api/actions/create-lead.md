# Create Lead with Myphoner

Creates a new lead in a Myphoner list.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/:listId/leads`
- **Base URL:** `https://{subdomain}.myphoner.com/api/v2`
- **Official documentation:** [Create Lead](https://www.myphoner.com/docs/api/#leads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `number` | yes | The Myphoner list ID. |
