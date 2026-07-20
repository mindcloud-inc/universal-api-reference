# Audit Log with Xodo Sign

Retrieves a document audit log from Xodo Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/document/:documentHash/audit_log`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Audit Log](https://eversign.com/api/documentation/methods#audit-log)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentHash` | path | `string` | yes | The unique document hash to fetch the audit log for. |
| `business_id` | query | `string` | yes | The Xodo Sign business ID that owns the document. |
