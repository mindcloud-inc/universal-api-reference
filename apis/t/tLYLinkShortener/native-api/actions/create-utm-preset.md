# Create UTM Preset with TLY Link Shortener

Creates a new UTM preset in TLY Link Shortener.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/link/utm-preset`
- **Base URL:** `https://api.t.ly`
- **Official documentation:** [Create UTM Preset](https://t.ly/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The preset name. |
| `source` | body | `string` | no | Optional UTM source value. |
| `medium` | body | `string` | no | Optional UTM medium value. |
| `campaign` | body | `string` | no | Optional UTM campaign value. |
| `content` | body | `string` | no | Optional UTM content value. |
| `term` | body | `string` | no | Optional UTM term value. |
