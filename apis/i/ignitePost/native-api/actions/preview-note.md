# Preview Note with IgnitePost

Retrieves preview image URLs for a note in IgnitePost.

## Endpoint

- **Method:** `POST`
- **Path:** `/preview`
- **Base URL:** `https://dashboard.ignitepost.com/api/v1`
- **Official documentation:** [Preview Note](https://dashboard.ignitepost.com/api-documentation#preview-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `font` | body | `string` | yes | IgnitePOST font key from the List Fonts action. |
| `message` | body | `string` | yes | Handwritten message content, up to 450 characters. Maximum length: 450. |
| `image` | body | `string` | yes | Front image key from List Default Images or a public image URL. |
| `image_inside` | body | `string` | yes | A stock image key or image URL for the card interior. |
| `image_backside` | body | `string` | yes | A stock image key or image URL for the card back. |
