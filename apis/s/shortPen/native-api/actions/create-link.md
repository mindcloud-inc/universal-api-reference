# Create Link with ShortPen

Creates a new link in ShortPen.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/generate`
- **Base URL:** `https://api.shortpen.com`
- **Official documentation:** [Create Link](https://shortpen.com/docs/api-reference/endpoint/generate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Destination URL that will be shortened. |
| `domain_id` | body | `number` | yes | ID of the domain that will host the short link. Use List Domains to find valid IDs. |
| `workspace_id` | body | `number` | no | Optional workspace override when the key can access multiple workspaces. |
| `title` | body | `string` | no | Optional human-friendly title for the link. |
| `custom_slug` | body | `string` | no | Branded slug to append instead of an auto-generated code. |
| `folder_id` | body | `number` | no | Existing folder to assign the link to. Use List Folders to find valid IDs. |
| `generate_qr` | body | `boolean` | no | Generate and return a QR code for the new link. |
| `enable_tracking` | body | `boolean` | no | Associate the link with a tracking pixel. Requires Pixel ID. |
| `pixel_id` | body | `number` | no | Pixel identifier used when tracking is enabled. Use List Pixels to find valid IDs. |
| `redirect_type` | body | `number` | no | HTTP redirect type. Use 301 or 302. |
| `link_cloak` | body | `boolean` | no | Cloak the destination URL. |
| `hide_referer` | body | `boolean` | no | Remove the referrer header for visitors. |
| `with_password` | body | `boolean` | no | Protect the link behind a password. |
| `url_password` | body | `string` | no | Password required when password protection is enabled. |
