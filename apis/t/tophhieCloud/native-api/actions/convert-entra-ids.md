# Convert Entra IDs with Tophhie Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/entra/convertid`
- **Base URL:** `https://api.tophhie.cloud`
- **Official documentation:** [Convert Entra IDs](https://api.tophhie.cloud/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | yes | Array of Entra Object IDs or SIDs to convert. Send multiple values as a array. |
