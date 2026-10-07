# List Payroll Summary Earnings with ADP

## Endpoint

- **Method:** `GET`
- **Path:** `payroll/v2/payroll-output/:outputId/associate-payment-summary/earnings`
- **Base URL:** `https://api.adp.com/`
- **Official documentation:** [List Payroll Summary Earnings](https://developers.adp.com/apis/api-explorer/hcm-offrg-wfn/hcm-offrg-wfn-payroll-payroll-outputs-v2-payroll-outputs?operation=GET%2Fpayroll%2Fv2%2Fpayroll-output%2F%7Boutput-id%7D%2Fassociate-payment-summary%2Fearnings#swagger)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputId` | path | `string` | yes | The payroll output identifier whose associate payment summary earnings should be returned. |
