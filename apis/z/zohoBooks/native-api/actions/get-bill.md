# Get Bill with Zoho Books

## Endpoint

- **Method:** `GET`
- **Path:** `/bills/:bill_id`
- **Base URL:** `https://www.zohoapis.com/books/v3`
- **Official documentation:** [Get Bill](https://www.zoho.com/books/api/v3/bills/#get-a-bill)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bill_id` | path | `string` | yes | Unique identifier of the bill. |
| `organization_id` | query | `string` | yes | ID of the organization. |
