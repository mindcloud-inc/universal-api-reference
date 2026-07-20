# Update Video Parameters with VdoCipher

Updates video parameters in VdoCipher.

## Endpoint

- **Method:** `POST`
- **Path:** `/videos/:videoId/params`
- **Base URL:** `https://dev.vdocipher.com/api`
- **Official documentation:** [Update Video Parameters](https://www.vdocipher.com/docs/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keys` | query | `string` | no | CSV value of keys |
| `values` | body | `string` | no | — |
| `videoId` | path | `string` | no | — |
