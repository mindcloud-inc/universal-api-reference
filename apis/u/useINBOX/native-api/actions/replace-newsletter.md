# Replace Newsletter with UseINBOX

Replaces an existing newsletter in UseINBOX.

## Endpoint

- **Method:** `PUT`
- **Path:** `/inbox/v1/newsletters/:id`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Replace Newsletter](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Newsletter ID from INBOX. |
| `subject` | body | `string` | yes | Newsletter subject. |
| `language` | body | `string` | yes | Newsletter language code such as en-US. |
| `htmlContent` | body | `string` | yes | Newsletter HTML content. |
