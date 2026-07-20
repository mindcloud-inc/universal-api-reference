# Update Extractor with Doctly

## Endpoint

- **Method:** `PUT`
- **Path:** `/e/:extractorId`
- **Base URL:** `https://api.doctly.ai/api/v1`
- **Official documentation:** [Update Extractor](https://docs.doctly.ai/api-reference/extractors/update)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extractorId` | path | `string` | yes | Unique extractor UUID to update. |
| `name` | body | `string` | no | New display name for the extractor. |
| `slug` | body | `string` | no | New unique URL-friendly slug for the extractor. |
