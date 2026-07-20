# Connect Person to Company with OneSuite

Connects a person to a company in OneSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/people/:people_id/company`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Connect Person to Company](https://rest-api.onesuite.io/#connect-people-to-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `people_id` | path | `string` | yes | People ID from the connect-people-to-company docs. |
| `companyId` | body | `string` | yes | Company ID to connect to the person. |
