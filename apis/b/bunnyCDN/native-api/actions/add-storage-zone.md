# Add Storage Zone with BunnyCDN

Creates a new storage zone in BunnyCDN.

## Endpoint

- **Method:** `POST`
- **Path:** `/storagezone`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Add Storage Zone](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | The name of the storage zone. |
| `Region` | body | `string` | yes | Primary storage region code. |
