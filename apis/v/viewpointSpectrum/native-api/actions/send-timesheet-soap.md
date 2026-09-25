# Send Timesheet (SOAP) with Viewpoint Spectrum

## Endpoint

- **Method:** `POST`
- **Path:** `ws/PreTimeCard`
- **Base URL:** `{url}:8482/`
- **Official documentation:** [Send Timesheet (SOAP)](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/add-vendor)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/xml; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchCode` | body | `string` | no | Discount percent. |
| `employeeCode` | body | `string` | no | Insurance certificate flag (Y/N). |
| `timeCardDate` | body | `string` | no | On hold flag (Y/N). |
| `department` | body | `string` | no | Default G/L Code. |
| `spectrumJob` | body | `string` | no | 1099 flag (Y/N). |
| `phase` | body | `string` | no | Alternate 1099 name. |
| `costType` | body | `string` | no | 1099 payment indicator. |
| `payType` | body | `string` | no | Social Security number. |
| `hours` | body | `string` | no | Federal ID number. |
| `wageCode` | body | `string` | no | Vendor email. |
| `costCenter` | body | `string` | no | Contact phone. |
| `equipmentCode` | body | `string` | no | — |
| `woNumber` | body | `string` | no | — |
| `woEquipment` | body | `string` | no | — |
| `woComponent` | body | `string` | no | — |
| `sCContract` | body | `string` | no | — |
| `pmWorkOrder` | body | `string` | no | — |
| `pmEquipment` | body | `string` | no | — |
| `pmAssembly` | body | `string` | no | — |
| `pmComponent` | body | `string` | no | — |
| `shiftCode` | body | `string` | no | — |
| `workLocality` | body | `string` | no | — |
| `notes` | body | `string` | no | — |
| `unionCode` | body | `string` | no | — |
| `classCode` | body | `string` | no | — |
| `tradeCode` | body | `string` | no | — |
| `taxLocality` | body | `string` | no | — |
| `taxState` | body | `string` | no | — |
| `workerCompCode` | body | `string` | no | — |
| `workCounty` | body | `string` | no | — |
| `locality` | body | `string` | no | — |
| `state` | body | `string` | no | — |
| `hoursEmployee` | body | `string` | no | — |
| `message` | body | `string` | no | — |
| `interCompanyCode` | body | `string` | no | — |
| `additionalJTDQuantity` | body | `string` | no | — |
| `workDate` | body | `string` | no | — |
| `payRateCode` | body | `string` | no | — |
| `crewNumber` | body | `string` | no | — |
| `costCategoryCode` | body | `string` | no | — |
| `payRate` | body | `string` | no | — |
