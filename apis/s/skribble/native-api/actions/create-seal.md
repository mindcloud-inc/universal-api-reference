# Create Seal with Skribble

Creates a sealed document in Skribble.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/seal`
- **Base URL:** `https://api.skribble.com`
- **Official documentation:** [Create Seal](https://api-doc.skribble.com/#72ed542c-7e2a-4140-ae03-27780b78acf7)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_name` | body | `string` | no | Optional business seal account name. |
| `content` | body | `string` | yes | The base64 encoded PDF content. |
| `visual_signature` | body | `object` | no | Optional visual seal payload including position and image. |
