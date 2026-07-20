# Create Location Batch With Path Options with Open Data DC

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2.2/locationbatch/:address_separator/:chunkSequnce_separator/:parallel`
- **Base URL:** `https://datagate.dc.gov/mar/open`
- **Official documentation:** [Create Location Batch With Path Options](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address_base64` | body | `string` | yes | Base64 encoded addresses in JSON object. |
| `address_separator` | path | `string` | yes | Address separator, default \|\|. |
| `chunkSequnce_separator` | path | `string` | yes | Chunk sequence separator, default colon. |
| `parallel` | path | `boolean` | yes | Whether to use parallel processing. |
