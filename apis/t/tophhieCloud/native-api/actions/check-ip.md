# Check IP with Tophhie Cloud

## Endpoint

- **Method:** `GET`
- **Path:** `/IPCheck`
- **Base URL:** `https://api.tophhie.cloud`
- **Official documentation:** [Check IP](https://api.tophhie.cloud/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | query | `string` | yes | The IP address to query. |
| `reverseCheck` | query | `boolean` | no | Whether to perform a reverse DNS lookup on the IP address. |
