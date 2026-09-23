# Send Timesheet (SOAP) with Viewpoint Spectrum

## Endpoint

- **Method:** `POST`
- **Path:** `ws/AddPRTimeCard`
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
