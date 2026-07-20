# Reactivate User with Othership

Reactivates an existing user in Othership.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/Users/:id`
- **Base URL:** `https://hwms-api.othership.com/api/v1/azure/scim`
- **Official documentation:** [Reactivate User](https://www.ietf.org/rfc/rfc7644)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The SCIM user identifier. |
