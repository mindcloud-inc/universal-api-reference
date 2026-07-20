# Update Ledger Instance with Particle

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/ledgers/:ledgerName/instances/:scopeValue`
- **Base URL:** `https://api.particle.io`
- **Official documentation:** [Update Ledger Instance](https://docs.particle.io/reference/cloud-apis/api/#set-the-ledger-instance-data)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `instance` | body | `object` | yes |
| `ledgerName` | path | `string` | yes |
| `scopeValue` | path | `string` | yes |
