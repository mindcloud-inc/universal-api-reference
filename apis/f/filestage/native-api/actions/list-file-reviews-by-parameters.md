# List File Reviews by Parameters with Filestage

Finds Filestage file reviews by parameter.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/reviews`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [List File Reviews by Parameters](https://developers.filestage.io/docs/api/mrkvlsdu1r54p-get-files-reviews-by-parameters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalId` | query | `string` | yes | `externalId` of the file |
| `stepId` | query | `string` | no | Step Id to filter results by. |
