# Get Transaction with Becon

Retrieves a transaction from Becon by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/transactions/:txid`
- **Base URL:** `https://external-api.bcon.global/api`
- **Official documentation:** [Get Transaction](https://bcon.global/integrations/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `txid` | path | `string` | yes | Blockchain transaction id to fetch. |
