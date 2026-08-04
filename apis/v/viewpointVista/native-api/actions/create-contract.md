# Create Contract with Viewpoint Vista

Create a contract

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/jc/2/data/contracts/actions/add`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Create Contract](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistajc2datajobsactionsadd)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CustRef` | path | `string` | no | — |
| `JCCo` | body | `number` | yes | Key to jc/jobs(JCCo, Job). 1 to 255. |
| `Contract` | body | `string` | yes | Key to jc/contracts(JCCo, Contract). Length <= 10. Maximum length: 10. |
| `Description` | body | `string` | no | Optional. If omitted, it will be defaulted based on Vista defaulting behavior. |
| `Department` | body | `string` | yes | — |
| `ContractStatus` | body | `number` | no | Allowed: 1, 2, 3 |
| `Notes` | body | `string` | no | Optional. If omitted, null will be defaulted. |
| `__custom_fields` | body | `object` | no | Add a property to this object for each user defined field to be set. Property name set to the user defined field name. |
| `ContractItems[]` | body | `array` | no | — |
| `Customer` | body | `number` | no | Key to ar/customers(CustGroup, Customer). CustGroup will be determined based on JCCo. Optional. If omitted, null will be defaulted. |
| `TaxCode` | body | `string` | no | — |
