# Change SM Work Order with Viewpoint Vista

Changes an existing Work Order record.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/actions/change`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Change SM Work Order](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistasm2datawork_ordersactionschange)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `__key` | body | `object` | no | — |
| `__key.SMWorkOrderID` | body | `number` | yes | Key sm/work_orders(SMWorkOrderID). |
| `Service Center` | body | `string` | no | Enter the Service center that this request is assigned to. |
| `Customer` | body | `number` | no | The SM Customer for this order.  **Required when `WorkOrderType` is `C-Customer`. |
| `Job` | body | `string` | no | The JC Job for this work order.  Required when `WorkOrderType` is `J-Job`. |
| `JCCo` | body | `number` | no | Enter JC Company.  Required when `WorkOrderType` is `J-Job` |
| `CustGroup` | body | `number` | no | — |
| `ServiceSite` | body | `string` | no | Enter a Site ID. |
| `WorkOrderQuote` | body | `string` | no | — |
| `WOStatus` | body | `number` | no | — |
| `ContactName` | body | `string` | no | Enter the contact name. |
| `ContactPhone` | body | `string` | no | Enter the contact phone. |
| `Description` | body | `string` | no | Enter a description of the request. |
| `Notes` | body | `string` | no | Enter a note about this work order. |
| `IsNew` | body | `boolean` | no | — |
| `CraftTemplate` | body | `number` | no | Enter a template code to identify craft/class pay rates. |
| `CostingMethod` | body | `list<string>` | no | Select a costing method. |
| `LeadTechnician` | body | `string` | no | Enter the lead technician. |
| `Reviewer` | body | `string` | no | Enter the Reviewer for this work. |
| `PRState` | body | `string` | no | Enter the State Code that identifies the location that work will be performed. |
| `PRLocalCode` | body | `string` | no | Enter the Payroll Local Code. |
| `UniqueAttchID` | body | `string` | no | — |
| `RequestedBy` | body | `string` | no | Enter the name of the person making this request. |
| `RequestedByPhone` | body | `string` | no | Enter the phone number of the person making this request. |
| `RequestedDate` | body | `string` | no | Enter the date that the request was made.  Format: `YYYY-MM-DD` |
| `RequestedTime` | body | `string` | no | Enter the time that the request was made.  Format: `HH:mm` |
| `Certified` | body | `list<string>` | no | Certified Payroll. For customer work orders only.  Options: - `Y`-Yes - `N`-No. |
| `CertifiedStartDate` | body | `string` | no | Enter the start date for certifieds.  Format: YYYY-MM-DD. |
| `EnteredBy` | body | `string` | no | The user that entered the work order. |
| `EnteredDateTime` | body | `string` | no | The date the work order was entered.  Format: `YYYY-MM-DD HH:mm` |
