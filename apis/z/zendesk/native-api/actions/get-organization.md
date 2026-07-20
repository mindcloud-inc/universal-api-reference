# Get Organization with Zendesk

Retrieves an organization from Zendesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:id.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [Get Organization](https://developer.zendesk.com/api-reference/ticketing/organizations/organizations/#show-organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Zendesk organization ID. |
