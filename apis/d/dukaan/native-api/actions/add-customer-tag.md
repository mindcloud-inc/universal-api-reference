# Add Customer Tag with Dukaan

Adds a tag to a customer in Dukaan.

## Endpoint

- **Method:** `POST`
- **Path:** `api/store/seller/:storeUuid/tags/`
- **Base URL:** `https://api.mydukaan.io`
- **Official documentation:** [Add Customer Tag](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storeUuid` | path | `string` | yes | Dukaan store UUID from developer settings. |
| `tag` | body | `number` | yes | Dukaan tag ID. |
| `object_id` | body | `string` | yes | Customer/store lead object ID to tag. |
| `content_type` | body | `string` | yes | Dukaan content type for the tagged object. |
