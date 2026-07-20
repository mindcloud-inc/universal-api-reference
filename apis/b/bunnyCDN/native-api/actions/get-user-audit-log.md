# Get User Audit Log with BunnyCDN

Retrieves BunnyCDN user audit log entries.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/audit/:date`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Get User Audit Log](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | path | `string` | yes | Audit log date in Bunny route format. |
