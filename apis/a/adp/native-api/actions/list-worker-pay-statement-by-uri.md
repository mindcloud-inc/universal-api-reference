# Get Worker Pay Statement with ADP

## Endpoint

- **Method:** `GET`
- **Path:** `payroll/v1/workers/:aoid/organizational-pay-statements/:payStatementId`
- **Base URL:** `https://api.adp.com/`
- **Official documentation:** [Get Worker Pay Statement](https://developers.adp.com/apis/api-explorer/hcm-offrg-wfn/hcm-offrg-wfn-payroll-pay-statements-v1-pay-statements?operation=GET%2Fpayroll%2Fv1%2Fworkers%2F%7Baoid%7D%2Forganizational-pay-statements%2F%7Bpay-statement-id%7D#swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aoid` | path | `string` | yes | The ADP associate object identifier for the worker whose pay statement should be returned. |
| `pay-statement-id` | path | `string` | yes | The pay statement identifier returned by List Worker Pay Statements. |
