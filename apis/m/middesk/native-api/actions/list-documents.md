# List documents for a business with Middesk

Retrieves business documents from your Middesk account.

## Endpoint

- **Method:** `GET`
- **Path:** `/businesses/:business_id/documents`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [List documents for a business](https://docs.middesk.com/reference/document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | path | `string` | yes | ID of the business whose documents you want to list. |
