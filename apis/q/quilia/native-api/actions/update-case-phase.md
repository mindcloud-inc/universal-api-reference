# Update Case Phase with Quilia

## Endpoint

- **Method:** `PATCH`
- **Path:** `cases/:id/phase`
- **Base URL:** `https://api.quilia.dev/v2`
- **Official documentation:** [Update Case Phase](https://api.quilia.dev/v2#tag/cases/PATCH/cases/%7Bid%7D/phase)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cms_data` | body | `string` | no | Any additional custom data for the case |
| `id` | path | `string` | yes | The unique identifier of the case to update |
| `phase` | body | `string` | yes | The new phase for the case |
| `updated_at` | body | `date` | no | The date and time when the case was last updated (ISO 8601 format) |
