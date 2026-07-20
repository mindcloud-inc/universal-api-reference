# Create Page with Papyrs

## Endpoint

- **Method:** `POST`
- **Path:** `/pages/create/`
- **Base URL:** `https://{subdomain}.papyrs.com/api/v1`
- **Official documentation:** [Create Page](https://papyrs.com/docs/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `string` | no | Optional folder path for the page. |
| `json[]` | body | `array<array>` | yes | The Papyrs page content JSON structure. |
| `layout[]` | body | `array<array>` | no | Optional page layout definition. |
| `notifications` | body | `object` | no | Optional notification settings keyed by user ID. |
| `permissions` | body | `object` | no | Optional permission settings keyed by user ID. |
| `title` | body | `string` | yes | The title of the new page. |
