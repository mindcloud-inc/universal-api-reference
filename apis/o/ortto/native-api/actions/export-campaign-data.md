# Export Campaign Data with Ortto

## Endpoint

- **Method:** `POST`
- **Path:** `/campaign/get-all`
- **Base URL:** `{apiBaseUrl}/v1`
- **Official documentation:** [Export Campaign Data](https://help.ortto.com/a-887-using-the-api-to-export-campaign-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | no | Single campaign type filter. |
| `types[]` | body | `array<string>` | no | List of campaign types to return. |
| `state` | body | `string` | no | Campaign state filter. |
| `folder_id` | body | `string` | no | Folder ID filter. |
| `campaign_ids[]` | body | `array<string>` | no | Specific campaign IDs to return. |
| `limit` | body | `number` | no | Maximum campaigns to return. |
| `offset` | body | `number` | no | Body offset for pagination. |
| `q` | body | `string` | no | Campaign name search query. |
| `sort_order` | body | `string` | no | Sort direction. |
| `sort` | body | `string` | no | Sort field. |
