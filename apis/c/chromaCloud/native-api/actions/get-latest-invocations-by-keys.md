# Get latest invocations by keys with Chroma Cloud

Retrieves the latest invocations by key from Chroma Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `https://sync.trychroma.com/api/v1/sources/:source_id/invocations/latest-by-keys`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Get latest invocations by keys](https://docs.trychroma.com/reference/sync-api/invocation/get-latest-invocations-by-keys)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `source_id` | path | `string` | yes |
| `object_keys[]` | body | `array<string>` | yes |
