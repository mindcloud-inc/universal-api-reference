# Create Customer Tag Definition with Dukaan

Creates a new customer tag definition in Dukaan.

## Endpoint

- **Method:** `POST`
- **Path:** `api/store/seller/:storeUuid/store-tags/`
- **Base URL:** `https://api.mydukaan.io`
- **Official documentation:** [Create Customer Tag Definition](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storeUuid` | path | `string` | yes | Dukaan store UUID from developer settings. |
| `tag_for` | body | `string` | yes | Dukaan object type this tag applies to. |
| `name` | body | `string` | yes | Customer tag name. |
