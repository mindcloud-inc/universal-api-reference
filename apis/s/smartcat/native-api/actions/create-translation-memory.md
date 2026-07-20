# Create Translation Memory with Smartcat

Creates a new translation memory in Smartcat.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/integration/v1/translationmemory`
- **Base URL:** `https://smartcat.ai`
- **Official documentation:** [Create Translation Memory](https://developers.smartcat.com/api/#create-an-empty-tm)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json-patch+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Translation memory name. |
| `sourceLanguage` | body | `string` | yes | Source language code. |
| `targetLanguages[]` | body | `array<string>` | no | Target language codes. |
| `description` | body | `string` | no | Translation memory description. |
| `clientId` | body | `string` | no | Client ID. |
