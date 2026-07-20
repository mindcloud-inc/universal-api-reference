# List Company Contacts with HubSpot

Retrieves contacts associated with a HubSpot company.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/objects/companies/:companyId/associations/contacts`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [List Company Contacts](https://developers.hubspot.com/docs/guides/api/crm/understanding-the-crm#retrieve-record-associations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `string` | yes | The company record ID. |
