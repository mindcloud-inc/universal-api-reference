# Save Page Highlights with Histre

Creates page highlights in Histre.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/highlight/`
- **Base URL:** `https://histre.com`
- **Official documentation:** [Save Page Highlights](https://histre.com/features/api/highlights/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Page URL where the highlight was created. |
| `title` | body | `string` | yes | Title of the page where the highlight was created. |
| `text` | body | `string` | yes | Highlighted text to save. |
| `color` | body | `string` | no | Optional highlight color. |
| `tweet` | body | `boolean` | no | Optional flag indicating the highlight comes from a tweet. |
| `extra` | body | `object` | no | Optional object of extra highlight details. |
| `note` | body | `string` | no | Optional note text attached to the highlight. |
