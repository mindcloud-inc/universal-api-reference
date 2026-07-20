# Get Inline Media with HelpSpace

Retrieves inline media from HelpSpace.

## Endpoint

- **Method:** `GET`
- **Path:** `/media/inline/{id}/{size}`
- **Base URL:** `https://api.helpspace.com/api/v1`
- **Official documentation:** [Get Inline Media](https://documentation.helpspace.com/api-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | HelpSpace inline media identifier. |
| `size` | path | `string` | no | Optional inline image size. Documented values are medium and large. |
