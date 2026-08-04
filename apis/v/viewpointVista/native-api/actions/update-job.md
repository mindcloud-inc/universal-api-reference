# Update Job with Viewpoint Vista

Update a Job based on a contract

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/jc/2/data/jobs/actions/change`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Update Job](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistajc2datajobsactionsadd)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `__key` | body | `object` | yes | KeyID: integer |
| `CustRef` | path | `string` | no | — |
| `Description` | body | `string` | no | Optional. If omitted, it will be defaulted based on Vista defaulting behavior. |
| `Contract` | body | `string` | no | Key to jc/contracts(JCCo, Contract). Length <= 10. Maximum length: 10. |
| `LiabTemplate` | body | `number` | no | Key to jc/liability_templates(JCCo, LiabTemplate). |
| `LockPhases` | body | `list<string>` | no | Optional. If omitted, N will be defaulted. Allowed: Y, N. Accepted values: `N`, `Y`. |
| `ProjectMgr` | body | `number` | no | Key to jc/project_managers(JCCo, ProjectMgr). Optional. If omitted, null will be defaulted. |
| `BidNumber` | body | `string` | no | Optional. If omitted, null will be defaulted. |
| `JobPhone` | body | `string` | no | Optional. If omitted, null will be defaulted. |
| `JobFax` | body | `string` | no | Optional. If omitted, null will be defaulted. |
| `MailAddress` | body | `string` | no | Optional. If omitted, null will be defaulted. |
| `MailCity` | body | `string` | no | Optional. If omitted, null will be defaulted. |
| `MailState` | body | `string` | no | Optional. If omitted, null will be defaulted. |
| `MailZip` | body | `string` | no | Optional. If omitted, null will be defaulted. |
| `MailAddress2` | body | `string` | no | Optional. If omitted, null will be defaulted. |
| `ShipAddress` | body | `string` | no | Optional. If omitted, null will be defaulted. |
| `ShipCity` | body | `string` | no | Optional. If omitted, null will be defaulted. |
| `ShipState` | body | `string` | no | Optional. If omitted, null will be defaulted. |
| `ShipZip` | body | `string` | no | Optional. If omitted, null will be defaulted. |
| `ShipAddress2` | body | `string` | no | Optional. If omitted, null will be defaulted. |
| `TaxCode` | body | `string` | no | Key to hq/tax_codes(TaxGroup, TaxCode). TaxGroup will be determined based on JCCo. Optional. If omitted, null will be defaulted. |
| `Notes` | body | `string` | no | Optional. If omitted, null will be defaulted. |
| `__custom_fields` | body | `object` | no | Add a property to this object for each user defined field to be set. Property name set to the user defined field name. |
| `RevGrpInv` | body | `string` | no | — |
