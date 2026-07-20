# Validate Routing Number with OnlineCheckWriter

Validates a bank routing number.

## Endpoint

- **Method:** `POST`
- **Path:** `/bankAccounts/routing-number/:routingNumber`
- **Base URL:** `https://test.onlinecheckwriter.com/api/v3`
- **Official documentation:** [Validate Routing Number](https://apiv3.onlinecheckwriter.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `routingNumber` | path | `string` | yes | The bank routing number to validate. |
