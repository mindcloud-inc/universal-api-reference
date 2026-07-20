# Update Organization with Zendesk

Updates an existing organization in Zendesk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/organizations/:id.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [Update Organization](https://developer.zendesk.com/api-reference/ticketing/organizations/organizations/#update-organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Zendesk organization ID. |
| `organization.name` | body | `string` | no | Updated organization name. |
| `organization.details` | body | `string` | no | Updated organization details. |
