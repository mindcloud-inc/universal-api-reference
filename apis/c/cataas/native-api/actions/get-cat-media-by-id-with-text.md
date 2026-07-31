# Get Cat Media By ID With Text with Cataas

## Endpoint

- **Method:** `GET`
- **Path:** `/cat/:catId/says/:text`
- **Base URL:** `https://cataas.com`
- **Official documentation:** [Get Cat Media By ID With Text](https://cataas.com/doc.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `catId` | path | `string` | yes | The ID of the cat media to retrieve. |
| `text` | path | `string` | yes | Text to render over this cat image. |
