# Get Card By Title with Writeathon

Retrieves a Writeathon card by title.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/users/{userId}/cards/get`
- **Base URL:** `https://api.writeathon.cn`
- **Official documentation:** [Get Card By Title](https://guide.writeathon.cn/help/tools/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The exact Writeathon card title to retrieve. |
