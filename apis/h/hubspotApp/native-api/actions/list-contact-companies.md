# List Contact Companies with HubSpot

Retrieves companies associated with a HubSpot contact.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/objects/contacts/:contactId/associations/companies`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [List Contact Companies](https://developers.hubspot.com/docs/guides/api/crm/understanding-the-crm#retrieve-record-associations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The contact record ID. |
