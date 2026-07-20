# Audit Log with Eversign

Retrieves a document audit log from Eversign.

## Endpoint

- **Method:** `GET`
- **Path:** `/document/:documentHash/audit_log`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Audit Log](https://eversign.com/api/documentation/methods)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `documentHash` | path | `string` | yes |
