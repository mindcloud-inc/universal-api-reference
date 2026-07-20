# Create Opportunity with OneSuite

Creates an opportunity in OneSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/opportunities`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Create Opportunity](https://rest-api.onesuite.io/#create-opportunity-with-all-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Opportunity name from the official create-opportunity docs. |
| `companyId` | body | `string` | no | Optional company ID to associate with the opportunity at creation time. |
| `pointOfContactId` | body | `string` | no | Optional point of contact people ID. |
