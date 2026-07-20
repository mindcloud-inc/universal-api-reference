# Create Seal with Skribble Sign

Creates a new seal in Skribble Sign.

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
| `content` | body | `string` | yes | The base64 encoded PDF content to seal. |
| `account_name` | body | `string` | no | Optional predefined company seal account name. |
| `visual_signature` | body | `object` | no | Optional visual seal placement payload. |
