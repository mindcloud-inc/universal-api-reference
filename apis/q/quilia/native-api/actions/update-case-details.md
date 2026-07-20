# Update Case Details with Quilia

## Endpoint

- **Method:** `PATCH`
- **Path:** `cases/:id`
- **Base URL:** `https://api.quilia.dev/v2`
- **Official documentation:** [Update Case Details](https://api.quilia.dev/v2#tag/cases/PATCH/cases/%7Bid%7D)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cms_data` | body | `string` | no | Additional custom data for the case |
| `id` | path | `string` | yes | The unique identifier of the case to update |
| `type` | body | `string` | no | The type/category of the case |
| `status` | body | `list<string>` | no | The status of the case Accepted values: `closed`, `open`. |
| `opened_at` | body | `date` | no | The date and time when the case was opened (ISO 8601 format) |
