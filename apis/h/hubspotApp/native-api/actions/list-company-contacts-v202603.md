# List Company Contacts v2026-03 with HubSpot

Retrieves company contacts from HubSpot using the 2026-03 API.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/2026-03/objects/companies/:companyId/associations/contacts`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [List Company Contacts v2026-03](https://developers.hubspot.com/docs/guides/api/crm/understanding-the-crm#retrieve-record-associations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `string` | yes | The company record ID. |
