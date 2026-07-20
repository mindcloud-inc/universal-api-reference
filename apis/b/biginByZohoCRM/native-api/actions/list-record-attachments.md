# List Record Attachments with Bigin by Zoho CRM

Retrieves attachments for a record in Bigin by Zoho CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/:moduleApiName/:recordId/Attachments`
- **Base URL:** `{api_domain}/bigin/v2`
- **Official documentation:** [List Record Attachments](https://www.bigin.com/developer/docs/apis/v2/get-attachments.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moduleApiName` | path | `list<string>` | yes | The API name of the parent module. |
| `recordId` | path | `string` | yes | The ID of the parent record. |
| `fields` | query | `string` | no | Comma-separated attachment fields to return. |
