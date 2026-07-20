# Get Record with Zoho Recruit

Retrieves a record from a Zoho Recruit module.

## Endpoint

- **Method:** `GET`
- **Path:** `/:moduleApiName/:recordId`
- **Base URL:** `https://recruit.zoho.com/recruit/v2`
- **Official documentation:** [Get Record](https://www.zoho.com/recruit/developer-guide/apiv2/get-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moduleApiName` | path | `string` | yes | The Zoho Recruit module API name that contains the record. |
| `recordId` | path | `string` | yes | The unique ID of the Zoho Recruit record. |
| `fields` | query | `string` | no | Comma-separated field API names to include in the single-record response. |
