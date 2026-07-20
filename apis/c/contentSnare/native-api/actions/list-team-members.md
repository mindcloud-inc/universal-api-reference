# List Team Members with Content Snare

Retrieves team members from Content Snare.

## Endpoint

- **Method:** `GET`
- **Path:** `/partner_api/v1/team_members`
- **Base URL:** `https://api.contentsnare.com`
- **Official documentation:** [List Team Members](https://api.contentsnare.com/partner_api/v1/documentation)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | String to search in the values specified in the parameter `q_by[]` |
| `q_by[]` | query | `array<string>` | no | Specifies list of values where string from the parameter `q` will be searched. If it isn't set then the default list is used.<br><b>Examples:</b> q_by[]=full_name&q_by[]=phone |
| `sort_by` | query | `string` | no | Specifies value for sorting |
| `sort_direction` | query | `string` | no | Specifies direction for sorting |
