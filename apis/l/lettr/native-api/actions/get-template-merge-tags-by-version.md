# Get Template Merge Tags By Version with Lettr

## Endpoint

- **Method:** `GET`
- **Path:** `/templates/:slug/merge-tags`
- **Base URL:** `https://app.lettr.com/api/`
- **Official documentation:** [Get Template Merge Tags By Version](https://docs.lettr.com/api-reference/templates/get-merge-tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Template slug. |
| `version` | query | `number` | no | Template version number. |
