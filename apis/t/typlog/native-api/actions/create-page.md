# Create Page with Typlog

Creates a new page in Typlog.

## Endpoint

- **Method:** `POST`
- **Path:** `/pages`
- **Base URL:** `https://api.typlog.com/v3`
- **Official documentation:** [Create Page](https://api.typlog.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | query | `number` | yes | Typlog site ID used to set the X-Site-Id header. |
| `title` | body | `string` | yes | Page title. |
| `slug` | body | `string` | yes | Page slug. |
| `lang` | body | `string` | yes | Page language code. |
| `format` | body | `string` | yes | Page content format. |
| `subtitle` | body | `string` | no | Page subtitle. |
| `visibility` | body | `string` | no | Page visibility. |
| `comment` | body | `string` | no | Comment setting. |
