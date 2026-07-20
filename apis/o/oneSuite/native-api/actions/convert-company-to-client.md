# Convert Company to Client with OneSuite

Converts a company to a client in OneSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/companies/:company_id/convert-to-client`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Convert Company to Client](https://rest-api.onesuite.io/#convert-company-to-client)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `string` | yes | Company ID from the OneSuite convert-company docs. |
| `message` | body | `string` | no | Optional invitation message for invited people. |
| `invitePeopleIds[]` | body | `array<string>` | no | Optional list of people IDs to invite to the client portal. Send multiple values as a array. |
