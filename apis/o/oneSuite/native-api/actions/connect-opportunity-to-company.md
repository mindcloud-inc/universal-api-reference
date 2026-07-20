# Connect Opportunity to Company with OneSuite

Connects an opportunity to a company in OneSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/opportunities/:opportunity_id/company`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Connect Opportunity to Company](https://rest-api.onesuite.io/#connect-opportunity-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opportunity_id` | path | `string` | yes | Opportunity ID from the connect-opportunity-company docs. |
| `companyId` | body | `string` | yes | Company ID to connect to the opportunity. |
