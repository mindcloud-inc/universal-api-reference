# Get Group with Qlik

Retrieves a group from your Qlik tenant.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/groups/:groupId`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Get Group](https://qlik.dev/apis/rest/groups/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | Qlik group ID. |
