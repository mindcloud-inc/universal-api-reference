# Screen Order with FraudLabs Pro

Screens an order for fraud in FraudLabs Pro.

## Endpoint

- **Method:** `POST`
- **Path:** `v2/order/screen`
- **Base URL:** `https://api.fraudlabspro.com/`
- **Official documentation:** [Screen Order](https://www.fraudlabspro.com/developer/api/screen-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | body | `string` | yes | IP address of the online transaction. |
