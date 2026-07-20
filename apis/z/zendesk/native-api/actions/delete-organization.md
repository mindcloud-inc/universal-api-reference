# Delete Organization with Zendesk

Deletes an existing organization from Zendesk.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/organizations/:id.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [Delete Organization](https://developer.zendesk.com/api-reference/ticketing/organizations/organizations/#delete-organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Organization ID |
