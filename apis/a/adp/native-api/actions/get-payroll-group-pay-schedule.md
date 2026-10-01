# Get Payroll Group Pay Schedule with ADP

## Endpoint

- **Method:** `GET`
- **Path:** `payroll/v1/pay-schedule/payroll-groups/:groupCode`
- **Base URL:** `https://api.adp.com/`
- **Official documentation:** [Get Payroll Group Pay Schedule](https://developers.adp.com/apis/api-explorer/hcm-offrg-wfn/hcm-offrg-wfn-payroll-payroll-group-pay-periods-v1-payroll-group-pay-periods?operation=GET%2Fpayroll%2Fv1%2Fpay-schedule%2Fpayroll-groups%2F%7Bgroup-code%7D#swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupCode` | path | `string` | yes | The payroll group code whose pay schedule and pay periods should be returned. |
