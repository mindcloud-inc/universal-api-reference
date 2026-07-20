# Start Charge with Monta

Starts a new charge in Monta.

## Endpoint

- **Method:** `POST`
- **Path:** `/charges`
- **Base URL:** `https://public-api.monta.com/api/v1`
- **Official documentation:** [Start Charge](https://docs.public-api.monta.com/reference/start-charge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chargePointId` | body | `number` | yes | ID of the charge point used to start this charge. |
