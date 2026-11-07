# Add G/L Journal Entry with Viewpoint Spectrum

Adds one line to a G/L journal entry batch in Spectrum. Lines sent with the same GUID form one balanced journal.

## Endpoint

- **Method:** `POST`
- **Path:** `ws/AddGLTrans`
- **Base URL:** `{url}:8482/`
- **API:** REST
- **Official documentation:** [Add G/L Journal Entry](https://help.trimble.com/doc/spectrum/spectrum/api-web-services/list-of-web-services/general-ledger-services/add-gl-journal-entries)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/xml; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `GUID` | body | `string` | no | Use the same GUID on every line of one journal, and a new GUID for the next journal. Spectrum generates one when blank. Maximum length: 36. |
| `Company_Code` | body | `string` | no | Spectrum company for this journal. Defaults to the connection's company. Every line of one journal must use the same company. Maximum length: 3. |
| `Transaction_Date` | body | `string` | yes | Calendar date as YYYY-MM-DD (or MM/DD/YYYY). Must be within the current G/L processing dates. The first line sets the journal header date. |
| `Journal_Desc` | body | `string` | yes | The first record determines the description for the journal header. Maximum length: 30. |
| `Journal_Remarks` | body | `string` | yes | The first record determines the remarks for the journal header. Maximum length: 100. |
| `GL_Account` | body | `string` | no | Enter the G/L account without dashes. Maximum length: 12. |
| `GL_Debit_Amount` | body | `number` | no | Positive values only. The complete journal batch must balance. Maximum length: 14. |
| `GL_Credit_Amount` | body | `number` | no | Positive values only. The complete journal batch must balance. Maximum length: 14. |
| `Cost_Center` | body | `string` | no | For cost center companies, required on the first record for the header and on non-direct G/L account lines. Maximum length: 10. |
| `Line_Reference` | body | `string` | no | Maximum length: 15. |
| `Job_Number` | body | `string` | no | Required for direct job cost accounts. Maximum length: 10. |
| `Phase_Code` | body | `string` | no | Enter the phase code without dashes. Required with Job Number and Cost Type for direct job cost accounts. Maximum length: 20. |
| `Cost_Type` | body | `string` | no | Required for direct job cost accounts. Maximum length: 3. |
| `Equipment_Code` | body | `string` | no | Required for direct equipment cost accounts. Maximum length: 10. |
| `Equipment_Cost_Category` | body | `string` | no | Required for direct equipment cost accounts. Maximum length: 4. |
| `Equipment_Work_Order` | body | `string` | no | Required, optional, or disallowed according to the equipment cost category data entry rule. Maximum length: 10. |
| `WO_Number` | body | `string` | no | Required for direct work order cost accounts. The work order must not be complete. Maximum length: 10. |
| `WO_Equipment` | body | `string` | no | Required when the work order installation requires equipment for work order transactions. Maximum length: 8. |
| `WO_Component` | body | `string` | no | Required when the installation requires components and the selected equipment has components. Maximum length: 2. |
| `WO_Contract` | body | `string` | no | Maximum length: 10. |
| `WO_Sellprice` | body | `number` | no | Maximum length: 14. |
| `Current_Record_Number` | body | `string` | no | Defined in AddGLTrans.jws but omitted from the help page. Confirm numbering with your Spectrum developer before batch testing. |
| `Total_Record_Count` | body | `string` | no | Defined in AddGLTrans.jws but omitted from the help page. Confirm batch usage with your Spectrum developer. |
| `IsBatchFlag` | body | `string` | no | Defined as a string in AddGLTrans.jws. Accepted values are not documented on the help page; confirm them before batch testing. |
