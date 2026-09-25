# Add Cash Receipts with Viewpoint Spectrum

## Endpoint

- **Method:** `POST`
- **Path:** `/ws/AddCash_Receipts`
- **Base URL:** `{url}:8482/`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/xml; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Company_Code` | body | `string` | yes |
| `Batch_Code` | body | `string` | no |
| `Customer_Code` | body | `string` | yes |
| `Transaction_Code` | body | `string` | no |
| `Reference_Number` | body | `string` | no |
| `Reference_Date` | body | `string` | no |
| `Transaction_Amount` | body | `string` | no |
| `ABA_Number` | body | `string` | no |
| `Invoice_Number` | body | `string` | no |
| `Invoice_Type` | body | `string` | no |
| `Payment_Amount` | body | `string` | no |
| `Discount_Taken` | body | `string` | no |
| `Cost_Center_Header` | body | `string` | no |
| `Overpayment_Flag` | body | `string` | no |
