# List Forums with Whop

Retrieves forums from Whop for a company.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/forums`
- **Base URL:** `https://api.whop.com`
- **Official documentation:** [List Forums](https://docs.whop.com/api-reference/forums/list-forums)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | query | `string` | yes | The unique identifier of the company to list forums for. |
