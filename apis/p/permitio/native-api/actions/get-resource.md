# Get Resource with Permit.io

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/schema/:projId/:envId/resources/:resourceId`
- **Base URL:** `https://api.permit.io`
- **Official documentation:** [Get Resource](https://api.permit.io/scalar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projId` | path | `string` | yes | Permit project identifier or key. |
| `envId` | path | `string` | yes | Permit environment identifier or key. |
| `resourceId` | path | `string` | yes | Permit resource identifier. |
