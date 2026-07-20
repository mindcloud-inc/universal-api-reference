# Get User with Permit.io

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/facts/:projId/:envId/users/:userId`
- **Base URL:** `https://api.permit.io`
- **Official documentation:** [Get User](https://api.permit.io/scalar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projId` | path | `string` | yes | Permit project identifier or key. |
| `envId` | path | `string` | yes | Permit environment identifier or key. |
| `userId` | path | `string` | yes | Permit user identifier. |
