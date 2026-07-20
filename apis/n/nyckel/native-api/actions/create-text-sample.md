# Create Text Sample with Nyckel

Creates a text sample in Nyckel.

## Endpoint

- **Method:** `POST`
- **Path:** `/functions/:functionId/samples`
- **Base URL:** `https://www.nyckel.com/v1`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `functionId` | path | `string` | yes | Nyckel function identifier. |
| `data` | body | `string` | yes | Sample text content. |
| `externalId` | body | `string` | no | Optional external identifier for the sample. |
| `annotation.labelId` | body | `string` | no | Optional label ID to assign as the annotation. |
| `annotation.labelName` | body | `string` | no | Optional label name to assign as the annotation. |
