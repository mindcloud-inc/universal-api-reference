# Save Episode Content with Typlog

Saves content for a Typlog episode.

## Endpoint

- **Method:** `POST`
- **Path:** `/episodes/[:id]/content`
- **Base URL:** `https://api.typlog.com/v3`
- **Official documentation:** [Save Episode Content](https://api.typlog.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the episode. |
| `siteId` | query | `number` | yes | Typlog site ID used to set the X-Site-Id header. |
| `content` | body | `string` | yes | Markdown or HTML content to save. |
| `auto` | body | `boolean` | no | Whether Typlog should auto process the content. |
