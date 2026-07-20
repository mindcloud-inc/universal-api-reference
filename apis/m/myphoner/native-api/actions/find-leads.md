# Find Leads with Myphoner

Finds leads in Myphoner by field values.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:listId/leads/find`
- **Base URL:** `https://{subdomain}.myphoner.com/api/v2`
- **Official documentation:** [Find Leads](https://www.myphoner.com/docs/api/#leads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `number` | yes | The Myphoner list ID. |
| `matchall` | query | `boolean` | no | When false, Myphoner matches any supplied field instead of all of them. |
