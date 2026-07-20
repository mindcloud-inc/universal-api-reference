# Get Media Version with Flotiq

Retrieves a media object version from Flotiq.

## Endpoint

- **Method:** `GET`
- **Path:** `/content/_media/{{id}}/version/{{versionId}}`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [Get Media Version](https://flotiq.com/docs/API/media/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Flotiq media object ID. |
| `versionId` | path | `string` | yes | The media version ID. |
