# Create Upload Intent with Sendible

## Endpoint

- **Method:** `POST`
- **Path:** `0.2/tw/uploads`
- **Base URL:** `https://api.sendible.com`
- **Official documentation:** [Create Upload Intent](https://support.sendible.com/hc/en-us)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source.contentType` | body | `string` | no | Original MIME type for file uploads. |
| `source.filename` | body | `string` | no | Original filename for file uploads. |
| `source.size` | body | `number` | no | Original file size in bytes. |
| `source.type` | body | `string` | yes | Upload source type, for example File or Url. |
| `source.url` | body | `string` | no | Remote URL when creating an upload intent from a URL source. |
