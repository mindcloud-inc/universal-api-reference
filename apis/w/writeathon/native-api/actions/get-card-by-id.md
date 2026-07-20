# Get Card By ID with Writeathon

Retrieves a Writeathon card by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/users/{userId}/cards/get`
- **Base URL:** `https://api.writeathon.cn`
- **Official documentation:** [Get Card By ID](https://guide.writeathon.cn/help/tools/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The Writeathon card ID to retrieve. |
