# Run echeck transaction with iframe with Nexiopay

## Endpoint

- **Method:** `GET`
- **Path:** `/pay/v3/processECheck`
- **Base URL:** `https://api.nexiopaysandbox.com`
- **Official documentation:** [Run echeck transaction with iframe](https://docs.nexiopay.com/reference/runechecktransactioniframe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | query | `string` | yes | One-time-use token returned by the token endpoint. |
