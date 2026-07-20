# Preview Template with SparkPost

## Endpoint

- **Method:** `POST`
- **Path:** `/templates/:id/preview`
- **Base URL:** `https://api.sparkpost.com/api/v1`
- **Official documentation:** [Preview Template](https://developers.sparkpost.com/api/templates/#templates-post-preview-a-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Template identifier. |
| `substitution_data` | body | `object` | no | Data passed to the template engine while previewing. |
