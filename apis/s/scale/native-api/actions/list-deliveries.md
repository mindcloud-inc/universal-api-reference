# List Deliveries with Scale

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/deliveries`
- **Base URL:** `https://api.scale.com`
- **Official documentation:** [List Deliveries](https://docs.genai.scale.com/v2/deliveries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `delivered_after` | query | `string` | no | Only return deliveries delivered after this timestamp. |
| `delivered_before` | query | `string` | no | Only return deliveries delivered before this timestamp. |
| `expand` | query | `string` | no | Comma-separated fields to expand in the response. |
| `project_id` | query | `string` | yes | Scale project identifier. Required in MindCloud for this action. |
| `project_name` | query | `string` | no | Optional alternative to Project ID when you want to scope by project name instead. |
