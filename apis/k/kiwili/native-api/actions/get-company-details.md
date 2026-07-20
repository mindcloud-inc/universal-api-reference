# Get Company Details with Kiwili

Retrieves details for a company in Kiwili.

## Endpoint

- **Method:** `GET`
- **Path:** `/company/:company_id`
- **Base URL:** `https://mindcloud.kiwili.com/api`
- **Official documentation:** [Get Company Details](https://api.kiwili.com/api/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `string` | yes | The Kiwili company ID. Use the string 0 for the active company profile. |
