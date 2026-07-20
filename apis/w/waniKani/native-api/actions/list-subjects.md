# List Subjects with WaniKani

Retrieves subjects from WaniKani.

## Endpoint

- **Method:** `GET`
- **Path:** `/subjects`
- **Base URL:** `https://api.wanikani.com/v2`
- **Official documentation:** [List Subjects](https://docs.api.wanikani.com/20170710/#get-all-subjects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | no | Comma-delimited subject IDs to include. |
| `types` | query | `string` | no | Comma-delimited subject types to include. |
| `slugs` | query | `string` | no | Comma-delimited subject slugs to include. |
| `levels` | query | `string` | no | Comma-delimited level numbers to include. |
| `hidden` | query | `boolean` | no | Whether to include hidden or visible subjects. |
| `updated_after` | query | `date` | no | Only return subjects updated after this ISO-8601 timestamp. |
