# Update Vendor (SOAP) with Viewpoint Spectrum

## Endpoint

- **Method:** `POST`
- **Path:** `ws/UpdateVendor`
- **Base URL:** `{url}:8482/`
- **Official documentation:** [Update Vendor (SOAP)](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/update-vendor)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/xml; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Vendor_Code` | body | `string` | yes | Vendor Code. |
| `Vendor_Name` | body | `string` | no | Vendor Name. |
| `Alpha_Sort` | body | `string` | no | Vendor Alpha Ref. |
| `Type` | body | `string` | no | Vendor Type. |
| `Our_Account_Number` | body | `string` | no | Account reference. |
| `Address_1` | body | `string` | no | Address 1. |
| `Address_2` | body | `string` | no | Address 2. |
| `City` | body | `string` | no | City. |
| `State` | body | `string` | no | State/province. |
| `Zip_Code` | body | `string` | no | Postal code. |
| `Addr_Country` | body | `string` | no | Country. |
| `Phone` | body | `string` | no | Phone Number. |
| `Fax_Phone` | body | `string` | no | Fax number. |
| `Vendor_Email` | body | `string` | no | Vendor email. |
| `Web_Site` | body | `string` | no | Website. |
| `Status` | body | `string` | no | Status: A, I, or N. |
| `Routing_Code1` | body | `string` | no | Routing Code for Invoice Approval. |
| `Routing_Limit` | body | `number` | no | Routing limit invoice approval. |
| `Routing_Code2` | body | `string` | no | Routing Code for Over Limit Invoice Approval. |
| `Use_Tax_Code` | body | `string` | no | Sales/Use Tax Code. |
| `Default_GL_Account` | body | `string` | no | Default G/L Code. |
| `Hold_Flag` | body | `string` | no | On hold flag (Y/N). |
| `Terms_Code` | body | `string` | no | Payment due terms (A or B only). |
| `Terms_Days` | body | `number` | no | Days Payment Due. |
| `Terms_Disc_Code` | body | `string` | no | Discount Due (A or B only). |
| `Terms_Disc_Days` | body | `number` | no | Days Discount Due. |
| `Terms_Disc_Percent` | body | `number` | no | Discount percent. |
| `Insurance_Cert_Flag` | body | `string` | no | Insurance certificate flag (Y/N). |
| `Insurance_Exp_Date` | body | `date` | no | Insurance expiration date. |
| `PO_Method` | body | `string` | no | Purchase order default method. |
| `Vendor_Status` | body | `string` | no | Payment method. |
| `Checking_Account_Code` | body | `string` | no | Electronic payment account code. |
| `Account_Type` | body | `string` | no | Electronic payment account type. |
| `ABA_Number` | body | `string` | no | Electronic payment ABA routing number. |
| `Send_1099_Flag` | body | `string` | no | 1099 flag (Y/N). |
| `Alt_1099_Name` | body | `string` | no | Alternate 1099 name. |
| `Fed_1099_Indicator` | body | `string` | no | 1099 payment indicator. |
| `Social_Sec_Number` | body | `string` | no | Social Security number. |
| `Fed_Id_Number` | body | `string` | no | Federal ID number. |
| `Override_Currency_Code` | body | `string` | no | Override Currency Code. |
| `Recipient_Type_Code` | body | `string` | no | Canadian T5018 recipient type code. |
| `Social_Insurance_Number` | body | `string` | no | Canadian T5018 social insurance number. |
| `Recipient_Account_Number` | body | `string` | no | Canadian T5018 recipient account number. |
| `Partnership_Filer_ID_Number` | body | `string` | no | Canadian T5018 partnership filer ID number. |
| `Alternate_T5018_Name` | body | `string` | no | Canadian T5018 alternate name. |
| `Individual_First_Name` | body | `string` | no | Canadian T5018 individual first name. |
| `Individual_Middle_Initial` | body | `string` | no | Canadian T5018 individual middle initial. |
| `Individual_Last_Name` | body | `string` | no | Canadian T5018 individual last name. |
