# View transactions with Nexiopay

## Endpoint

- **Method:** `GET`
- **Path:** `/transaction/v3`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [View transactions](https://docs.nexiopay.com/reference/viewtransactions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | query | `date` | no | Start date for transaction reporting, for example 2019-02-13. |
| `endDate` | query | `date` | no | End date for transaction reporting, for example 2019-02-19. |
