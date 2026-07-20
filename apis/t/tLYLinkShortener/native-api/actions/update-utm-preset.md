# Update UTM Preset with TLY Link Shortener

Updates an existing UTM preset in TLY Link Shortener.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/link/utm-preset/:id`
- **Base URL:** `https://api.t.ly`
- **Official documentation:** [Update UTM Preset](https://t.ly/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The preset ID to update. |
| `name` | body | `string` | yes | The preset name. |
| `source` | body | `string` | no | Optional UTM source value. |
| `medium` | body | `string` | no | Optional UTM medium value. |
| `campaign` | body | `string` | no | Optional UTM campaign value. |
| `content` | body | `string` | no | Optional UTM content value. |
| `term` | body | `string` | no | Optional UTM term value. |
