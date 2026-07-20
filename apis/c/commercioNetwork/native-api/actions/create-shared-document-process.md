# Create Shared Document Process with CommercioNetwork

Creates a shared document process in CommercioNetwork.

## Endpoint

- **Method:** `POST`
- **Path:** `/sharedoc/process`
- **Base URL:** `https://dev-api.commercio.app/v1`
- **Official documentation:** [Create Shared Document Process](https://docs.commercio.network/app_developers/commercioapi-sharedoc.html#send-a-sharedoc-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content_uri` | body | `string` | yes | The document URI recorded in Commercio. |
| `hash` | body | `string` | yes | The SHA-256 hash of the document content. |
| `hash_algorithm` | body | `string` | yes | The hashing algorithm used for the document hash. |
| `recipients[]` | body | `array<string>` | yes | One or more recipient wallet addresses in DID format. |
