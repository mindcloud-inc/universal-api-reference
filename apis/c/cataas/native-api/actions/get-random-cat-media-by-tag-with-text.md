# Get Random Cat Media By Tag With Text with Cataas

## Endpoint

- **Method:** `GET`
- **Path:** `/cat/:tag/says/:text`
- **Base URL:** `https://cataas.com`
- **Official documentation:** [Get Random Cat Media By Tag With Text](https://cataas.com/doc.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag` | path | `string` | yes | Return a random cat matching this tag. |
| `text` | path | `string` | yes | Text to render over the tagged cat image. |
