# List App Version Update Candidates with mittwald

Retrieves app version update candidates from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/apps/:appId/versions/:baseAppVersionId/update-candidates`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [List App Version Update Candidates](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | The unique identifier of the app. |
| `baseAppVersionId` | path | `string` | yes | The unique identifier of the base app version. |
