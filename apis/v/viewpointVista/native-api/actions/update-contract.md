# Update Contract with Viewpoint Vista

Update a contract

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/jc/2/data/contracts/actions/change`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Update Contract](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistajc2datajobsactionsadd)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `__key` | body | `object` | yes | — |
| `CustRef` | path | `string` | no | — |
| `Description` | body | `string` | no | Optional. If omitted, it will be defaulted based on Vista defaulting behavior. |
| `Department` | body | `string` | no | — |
| `ContractStatus` | body | `number` | no | Allowed: 1, 2, 3 |
| `Notes` | body | `string` | no | Optional. If omitted, null will be defaulted. |
| `ContractItems[]` | body | `array` | no | — |
| `Customer` | body | `number` | no | Key to ar/customers(CustGroup, Customer). CustGroup will be determined based on JCCo. Optional. If omitted, null will be defaulted. |
| `TaxCode` | body | `string` | no | — |
| `__custom_fields` | body | `object` | no | Add a property to this object for each user defined field to be set. Property name set to the user defined field name. |
