# Create Team with SuperSend

Creates a new team in SuperSend.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Create Team](https://docs.supersend.io/docs/team)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `domain` | body | `string` | no |
| `logo` | body | `string` | no |
| `about` | body | `string` | no |
| `meeting_link` | body | `string` | no |
| `meeting_link_text` | body | `string` | no |
| `auto_placement_testing` | body | `boolean` | no |
