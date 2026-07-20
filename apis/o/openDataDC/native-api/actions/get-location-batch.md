# Get Location Batch with Open Data DC

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2.2/locationbatch/:address_base64/:address_separator/:chunkSequnce_separator/:parallel`
- **Base URL:** `https://datagate.dc.gov/mar/open`
- **Official documentation:** [Get Location Batch](https://datagate.dc.gov/mar/open/swagger/v2.2/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address_base64` | path | `string` | yes | Base64 encoded address string. |
| `address_separator` | path | `string` | yes | Address separator, default \|\|. |
| `chunkSequnce_separator` | path | `string` | yes | Chunk sequence separator, default colon. |
| `parallel` | path | `boolean` | yes | Whether to use parallel processing. |
