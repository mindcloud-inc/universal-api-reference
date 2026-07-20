# Update Link with ShortPen

Updates an existing link in ShortPen.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/links`
- **Base URL:** `https://api.shortpen.com`
- **Official documentation:** [Update Link](https://shortpen.com/docs/api-reference/endpoint/edit-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url_id` | body | `number` | yes | ID of the existing link to update. |
| `url` | body | `string` | no | New destination URL for the link. |
| `domain_id` | body | `number` | no | ID of the domain that should host the link. Use List Domains to find valid IDs. |
| `workspace_id` | body | `number` | no | Optional workspace override when updating the link. |
| `title` | body | `string` | no | Optional human-friendly title for the link. |
| `custom_slug` | body | `string` | no | Branded slug to apply to the link. |
| `folder_id` | body | `number` | no | Existing folder to assign the link to. Use List Folders to find valid IDs. |
| `generate_qr` | body | `boolean` | no | Generate or regenerate a QR code for the link. |
| `enable_tracking` | body | `boolean` | no | Associate the link with a tracking pixel. Requires Pixel ID. |
| `pixel_id` | body | `number` | no | Pixel identifier used when tracking is enabled. Use List Pixels to find valid IDs. |
| `redirect_type` | body | `number` | no | HTTP redirect type. Use 301 or 302. |
| `link_cloak` | body | `boolean` | no | Cloak the destination URL. |
| `hide_referer` | body | `boolean` | no | Remove the referrer header for visitors. |
| `with_password` | body | `boolean` | no | Protect the link behind a password. |
| `url_password` | body | `string` | no | Password required when password protection is enabled. |
