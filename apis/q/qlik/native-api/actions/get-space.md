# Get Space with Qlik

Retrieves a space from your Qlik tenant.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/spaces/:spaceId`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Get Space](https://qlik.dev/apis/rest/spaces/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Qlik space ID. |
