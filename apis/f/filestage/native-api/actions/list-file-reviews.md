# List File Reviews with Filestage

Retrieves reviews for a Filestage file.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/{fileId}/reviews`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [List File Reviews](https://developers.filestage.io/docs/api/bb3tlfor3cocg-get-file-reviews)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stepId` | query | `string` | no | Step Id to filter results by. |
| `fileId` | path | `string` | yes | File Id |
