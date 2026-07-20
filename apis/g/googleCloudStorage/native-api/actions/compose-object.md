# Compose Object with Google Cloud Storage

Composes multiple objects into one in Google Cloud Storage.

## Endpoint

- **Method:** `POST`
- **Path:** `/storage/v1/b/:destinationBucket/o/:destinationObject/compose`
- **Base URL:** `https://storage.googleapis.com`
- **Official documentation:** [Compose Object](https://docs.cloud.google.com/storage/docs/json_api/v1/objects/compose)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destinationBucket` | path | `list<string>` | yes | Bucket to create the composed object in. |
| `destinationObject` | path | `string` | yes | Destination object name. |
| `sourceObjects[]` | body | `array<object>` | yes | Source object entries to compose. |
| `sourceObjects[].name` | body | `string` | yes | Name of a source object to compose. All source objects must be in the selected destination bucket. |
| `sourceObjects[].generation` | body | `string` | no | Generation of the source object to use. |
| `sourceObjects[].objectPreconditions` | body | `object` | no | Conditions that must be met for the source object to be used in composition. |
| `sourceObjects[].objectPreconditions.ifGenerationMatch` | body | `string` | no | Only compose if the source object generation matches this value. |
| `deleteSourceObjects` | body | `boolean` | no | Whether to delete source objects after composition. |
