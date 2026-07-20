# Create Annotation with Rossum

Creates a new annotation in Rossum.

## Endpoint

- **Method:** `POST`
- **Path:** `/annotations`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Create Annotation](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | body | `string` | yes | Document URL. |
| `queue` | body | `string` | yes | Target queue URL. |
