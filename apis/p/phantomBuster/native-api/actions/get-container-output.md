# Get Container Output with PhantomBuster

Retrieves container output from PhantomBuster.

## Endpoint

- **Method:** `GET`
- **Path:** `/containers/fetch-output`
- **Base URL:** `https://api.phantombuster.com/api/v2`
- **Official documentation:** [Get Container Output](https://hub.phantombuster.com/reference/get_containers-fetch-output)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | The PhantomBuster container ID whose latest output you want. |
| `mode` | query | `list` | no | Accepted values: `json`, `raw`. |
