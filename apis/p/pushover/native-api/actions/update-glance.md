# Update Glance with Pushover

## Endpoint

- **Method:** `POST`
- **Path:** `/glances.json`
- **Base URL:** `https://api.pushover.net/1`
- **Official documentation:** [Update Glance](https://pushover.net/api/glances#update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | query | `string` | yes | Pushover user key for the widget owner. |
| `device` | query | `string` | no | Optional device name to target a specific widget. |
| `title` | query | `string` | no | Short description shown for the glance data. Maximum length: 100. |
| `text` | query | `string` | no | Main glance text shown on most screens. Maximum length: 100. |
| `subtext` | query | `string` | no | Secondary line of glance data. Maximum length: 100. |
| `count` | query | `number` | no | Integer count shown on smaller screens. |
| `percent` | query | `number` | no | Progress percentage from 0 through 100. |
