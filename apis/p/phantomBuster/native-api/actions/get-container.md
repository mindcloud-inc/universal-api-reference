# Get Container with PhantomBuster

Retrieves a container from PhantomBuster.

## Endpoint

- **Method:** `GET`
- **Path:** `/containers/fetch`
- **Base URL:** `https://api.phantombuster.com/api/v2`
- **Official documentation:** [Get Container](https://hub.phantombuster.com/reference/get_containers-fetch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | The PhantomBuster container ID to fetch. |
| `withNewerAndOlderContainerId` | query | `string` | no | — |
| `withOutput` | query | `string` | no | — |
| `withResultObject` | query | `string` | no | — |
| `withRuntimeEvents` | query | `string` | no | — |
