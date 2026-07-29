# Insert Company with Rillion Prime Web Service

Insert a company into the Prime register queue.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Company` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Company section. |
| `Company.Company` | body | `list<string>` | yes | Company ID |
| `Company.Name` | body | `string` | yes | Trade name |
| `Company.ValidTo` | body | `date` | no | Can receive invoices until this date |
| `Company.InvoiceSeries` | body | `string` | no | FK to invoice number series |
| `Company.ArrivalType` | body | `number` | no | When is the invoice to be preliminarily recorded in the ERP system: 0=Never; 1=When it is sent to the first person in the flow; 2=When the first person in the flow has approved it |
| `Company.BaseCurrency` | body | `string` | no | Currency for accounting purpose |
| `Company.Erp` | body | `string` | no | Belongs to this ERP system if several used (used for integration purposes) |
| `Company.Group1` | body | `string` | no | Free field of Type 1 |
| `Company.Group2` | body | `string` | no | Free field of Type 2 |
| `Company.Group3` | body | `string` | no | Free field of Type 3 |
| `Company.Remove` | body | `number` | no | — |
| `Company.AllocationSetting` | body | `number` | no | Method of distribution: 0=Distribute by From and To date; 1=Distribute by distribution type |
| `Company.CalculateVATAmountOnCostRow` | body | `boolean` | no | — |
| `TransferFromQueue` | body | `boolean` | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. |
