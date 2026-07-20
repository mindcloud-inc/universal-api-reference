# Cancel Emergency Receipt with Pushover

## Endpoint

- **Method:** `POST`
- **Path:** `/receipts/:receipt/cancel.json`
- **Base URL:** `https://api.pushover.net/1`
- **Official documentation:** [Cancel Emergency Receipt](https://pushover.net/api/receipts#cancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `receipt` | path | `string` | yes | Emergency notification receipt to cancel. |
