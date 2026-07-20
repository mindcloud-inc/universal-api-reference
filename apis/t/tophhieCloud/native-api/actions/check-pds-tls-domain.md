# Check PDS TLS Domain with Tophhie Cloud

Verifies PDS TLS eligibility for a domain or handle in Tophhie Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/pds/tls-check`
- **Base URL:** `https://api.tophhie.cloud`
- **Official documentation:** [Check PDS TLS Domain](https://api.tophhie.cloud/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Domain name or handle to check for TLS certificate validation. |
