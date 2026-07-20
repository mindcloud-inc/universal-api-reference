# List Charges with Monta

Retrieves charges from Monta.

## Endpoint

- **Method:** `GET`
- **Path:** `/charges`
- **Base URL:** `https://public-api.monta.com/api/v1`
- **Official documentation:** [List Charges](https://docs.public-api.monta.com/reference/get-charges)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chargePointId` | query | `number` | no | Only return charges for this charge point ID. |
| `state` | query | `list<string>` | no | Only return charges in this state. Accepted values: `charging`, `completed`, `paused`, `reserved`, `scheduled`, `starting`, `stopped`, `stopping`. |
| `fromDate` | query | `date` | no | Only return charges created at or after this ISO 8601 date-time. |
| `toDate` | query | `date` | no | Only return charges created at or before this ISO 8601 date-time. |
