# Create Vendor with Viewpoint Spectrum

## Endpoint

- **Method:** `POST`
- **Path:** `ws/AddVendor`
- **Base URL:** `{url}:8482/`
- **Official documentation:** [Create Vendor](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-payable-services/add-vendor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Vendor_Code` | body | `string` | yes | Vendor Code. |
| `Vendor_Name` | body | `string` | yes | Vendor Name. |
| `Alpha_Sort` | body | `string` | yes | Vendor Alpha Ref. |
| `Type` | body | `string` | no | Vendor Type. |
| `Address_1` | body | `string` | no | Address 1. |
| `Address_2` | body | `string` | no | Address 2. |
| `Address_3` | body | `string` | no | City. |
| `State` | body | `string` | no | State/province. |
| `Zip_Code` | body | `string` | no | Postal code. |
| `Phone` | body | `string` | no | Phone Number. |
| `Fax_Phone` | body | `string` | no | Fax number. |
| `Contact_Name` | body | `string` | no | Contact Name. |
| `Our_Account_Number` | body | `string` | no | Account reference. |
| `Terms_Code` | body | `string` | yes | Payment due terms (A or B only). |
| `Terms_Days` | body | `number` | yes | Days Payment Due. |
| `Terms_Disc_Code` | body | `string` | yes | Discount Due (A or B only). |
| `Terms_Disc_Days` | body | `number` | no | Days Discount Due. |
| `Terms_Disc_Percent` | body | `number` | no | Discount percent. |
| `Insurance_Cert_Flag` | body | `string` | no | Insurance certificate flag (Y/N). |
| `Insurance_Exp_Date` | body | `date` | no | Insurance expiration date. |
| `Hold_Flag` | body | `string` | no | On hold flag (Y/N). |
| `Default_GL_Account` | body | `string` | no | Default G/L Code. |
| `Use_Tax_Code` | body | `string` | no | Sales/Use Tax Code. |
| `Send_1099_Flag` | body | `string` | no | 1099 flag (Y/N). |
| `Alt_1099_Name` | body | `string` | no | Alternate 1099 name. |
| `Fed_1099_Indicator` | body | `string` | no | 1099 payment indicator. |
| `Social_Sec_Number` | body | `string` | no | Social Security number. |
| `Fed_Id_Number` | body | `string` | no | Federal ID number. |
| `Vendor_Email` | body | `string` | no | Vendor email. |
| `Contact_Phone` | body | `string` | no | Contact phone. |
