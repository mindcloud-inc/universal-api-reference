# Create Payroll Batch with ADP

## Endpoint

- **Method:** `POST`
- **Path:** `events/payroll/v1/pay-data-input.modify`
- **Base URL:** `https://api.adp.com/`
- **Official documentation:** [Create Payroll Batch](https://developers.adp.com/apis/api-explorer/hcm-offrg-wfn/hcm-offrg-wfn-payroll-pay-data-input-v1-pay-data-input?operation=POST%2Fevents%2Fpayroll%2Fv1%2Fpay-data-input.modify#swagger)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyCode` | body | `string` | yes |
| `entry[].additionalPayCodes[].payCode` | body | `string` | no |
| `entry[].fileNumber` | body | `string` | no |
| `batchID` | body | `string` | yes |
| `entry[].additionalPayCodes[].hours` | body | `number` | no |
| `entry[].associateOID` | body | `string` | no |
| `entry[]` | body | `array` | no |
| `entry[].regularHours` | body | `number` | no |
| `entry[].overTimeHours` | body | `number` | no |
| `entry[].ptoHours` | body | `number` | no |
| `entry[].holidayHours` | body | `number` | no |
| `entry[].additionalPayCodes[]` | body | `array` | no |
