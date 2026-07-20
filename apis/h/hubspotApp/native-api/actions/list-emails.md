# List Emails with HubSpot

Retrieves email activities from HubSpot.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/objects/emails`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [List Emails](https://developers.hubspot.com/docs/api-reference/crm-emails-v3/basic/get-crm-v3-objects-emails)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `properties[]` | query | `array<string>` | no | Properties to return for each email. |
| `propertiesWithHistory[]` | query | `array<string>` | no | Properties to return with version history. |
| `associations[]` | query | `array<string>` | no | Associated object types to include. |
| `archived` | query | `boolean` | no | Whether to include archived emails. |
