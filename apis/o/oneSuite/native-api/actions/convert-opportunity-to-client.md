# Convert Opportunity to Client with OneSuite

Converts an opportunity to a client in OneSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/opportunities/:opportunity_id/convert-to-client`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Convert Opportunity to Client](https://rest-api.onesuite.io/#convert-opportunity-to-client)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opportunity_id` | path | `string` | yes | Opportunity ID from the convert-opportunity docs. |
| `companyId` | body | `string` | no | Optional company ID if different from the opportunity's connected company. |
| `message` | body | `string` | no | Optional invitation message for invited people. |
