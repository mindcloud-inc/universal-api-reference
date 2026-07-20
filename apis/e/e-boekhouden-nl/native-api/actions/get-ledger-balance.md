# Get Ledger Balance with e-Boekhouden.nl

Retrieves a ledger balance from e-Boekhouden.nl.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/ledger/:id/balance`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [Get Ledger Balance](https://api.e-boekhouden.nl/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `costCenterId` | query | `number` | no | The ID of the cost center. |
| `from` | query | `date` | no | Show the balance starting from this date. When provided, the resulting balance is the difference over the period, rather than the actual balance. |
| `to` | query | `date` | no | Shows the active balance at this date. This date is inclusive. |
| `id` | path | `number` | yes | — |
