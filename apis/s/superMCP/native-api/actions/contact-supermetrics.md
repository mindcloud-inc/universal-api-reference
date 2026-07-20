# Contact Supermetrics with SuperMCP

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp/contact_supermetrics`
- **Base URL:** `https://mcp.supermetrics.com`
- **Official documentation:** [Contact Supermetrics](https://mcp.supermetrics.com/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Request type, such as feedback, support, or sales. |
| `subject` | body | `string` | yes | Contact request subject. |
| `message` | body | `string` | yes | Contact request message. |
| `category` | body | `string` | no | Optional request category. |
| `ds_id` | body | `string` | no | Optional related Supermetrics data source ID. |
| `company` | body | `string` | no | Optional company name. |
