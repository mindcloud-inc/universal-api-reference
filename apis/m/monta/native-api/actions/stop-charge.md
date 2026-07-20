# Stop Charge with Monta

Stops an active charge in Monta.

## Endpoint

- **Method:** `POST`
- **Path:** `/charges/{chargeId}/stop`
- **Base URL:** `https://public-api.monta.com/api/v1`
- **Official documentation:** [Stop Charge](https://docs.public-api.monta.com/reference/stop-charge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chargeId` | path | `number` | yes | ID of the charge to stop. |
