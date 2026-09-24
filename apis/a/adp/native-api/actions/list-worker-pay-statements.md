# List Worker Pay Statements with ADP

## Endpoint

- **Method:** `GET`
- **Path:** `payroll/v1/workers/:aoid/organizational-pay-statements`
- **Base URL:** `https://api.adp.com/`
- **Official documentation:** [List Worker Pay Statements](https://developers.adp.com/apis/api-explorer/hcm-offrg-wfn/hcm-offrg-wfn-payroll-pay-statements-v1-pay-statements?operation=GET%2Fpayroll%2Fv1%2Fworkers%2F%7Baoid%7D%2Forganizational-pay-statements#swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aoid` | path | `string` | yes | The ADP associate object identifier for the worker whose pay statements should be returned. |
