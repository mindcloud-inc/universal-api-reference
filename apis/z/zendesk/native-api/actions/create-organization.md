# Create Organization with Zendesk

Creates a new organization in Zendesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [Create Organization](https://developer.zendesk.com/api-reference/ticketing/organizations/organizations/#create-organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization.name` | body | `string` | yes | Name of the organization. |
| `organization.details` | body | `string` | no | Optional details for the organization. |
