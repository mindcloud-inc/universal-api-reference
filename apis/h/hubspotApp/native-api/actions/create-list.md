# Create List with HubSpot

Creates a new list in HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/lists`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Create List](https://developers.hubspot.com/docs/api-reference/crm-lists-v3/lists/post-crm-v3-lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | New list name. |
| `objectTypeId` | body | `string` | yes | HubSpot object type ID (0-1 for contacts). |
| `processingType` | body | `string` | yes | List processing type (for example MANUAL). |
