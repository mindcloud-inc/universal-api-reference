# Get Custom Object Record with Zoho CRM

## Endpoint

- **Method:** `GET`
- **Path:** `/:moduleApiName/:recordId`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Get Custom Object Record](https://www.zoho.com/crm/developer/docs/api/v8/get-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moduleApiName` | path | `list<string>` | yes | Select the exact Zoho API name. Discovery includes standard modules too; custom modules have generatedType=custom. |
| `recordId` | path | `string` | yes | — |
