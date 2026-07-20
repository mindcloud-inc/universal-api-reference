# Convert Markdown with Mythic Text

## Endpoint

- **Method:** `POST`
- **Path:** `/convert`
- **Base URL:** `https://mythictext-api.vercel.app`
- **Official documentation:** [Convert Markdown](https://mythictext.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `markdown` | body | `string` | yes | Markdown content to convert. |
| `target` | body | `string` | yes | Output target. Supported values include html, web, email, gmail, googledocs, wordpress, markdown, and pdf. |
