# Create Newsletter with UseINBOX

Creates a newsletter in UseINBOX.

## Endpoint

- **Method:** `POST`
- **Path:** `/inbox/v1/newsletters`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Create Newsletter](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject` | body | `string` | yes | Newsletter subject. |
| `language` | body | `string` | yes | Newsletter language code such as en-US. |
| `htmlContent` | body | `string` | yes | Newsletter HTML content. |
