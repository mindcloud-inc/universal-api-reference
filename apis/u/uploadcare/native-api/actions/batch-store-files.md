# Batch Store Files with Uploadcare

Stores multiple files in Uploadcare storage.

## Endpoint

- **Method:** `PUT`
- **Path:** `/files/storage/`
- **Base URL:** `https://api.uploadcare.com`
- **Official documentation:** [Batch Store Files](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File/operation/filesStoring)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuids[]` | body | `array<string>` | yes | List of Uploadcare file UUIDs to store. |
