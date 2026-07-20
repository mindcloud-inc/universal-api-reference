# Create Company with OneSuite

Creates a company in OneSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/companies`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Create Company](https://rest-api.onesuite.io/#create-company-with-all-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Company name from the official OneSuite create-company docs. |
| `opportunityId` | body | `string` | no | Optional opportunity ID to connect when creating the company. |
