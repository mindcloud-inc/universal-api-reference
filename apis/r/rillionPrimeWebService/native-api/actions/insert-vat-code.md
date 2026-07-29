# Insert VAT Code with Rillion Prime Web Service

Insert a VAT code into the Prime register queue.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `VatCode` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, VatCode section. |
| `VatCode.Company` | body | `list<string>` | no | Company to which VAT code belongs |
| `VatCode.VatCode` | body | `string` | yes | VAT code |
| `VatCode.Name` | body | `string` | yes | VAT code name |
| `VatCode.ValidTo` | body | `date` | no | A valid to date for vatcodes |
| `VatCode.Account` | body | `string` | no | VAT account to which VAT code belongs |
| `VatCode.Percentage` | body | `number` | no | VAT rate |
| `VatCode.VatDeductionAccount` | body | `string` | no | Account for VAT remainder |
| `VatCode.Group1` | body | `string` | no | Free group 1 |
| `VatCode.Group2` | body | `string` | no | Free group 2 |
| `VatCode.Group3` | body | `string` | no | Free group 3 |
| `VatCode.KeyType` | body | `number` | no | Is the company included in the primary key for the record: 0=No; 1=Yes |
| `VatCode.ExternalId` | body | `string` | no | — |
| `VatCode.ExternalSource` | body | `string` | no | — |
| `VatCode.FromDate` | body | `date` | no | From invoice date the VAT percentage shall be used. Support of SAF-T |
| `VatCode.DeductionalVatPercentage` | body | `number` | no | Percentage of deductible VAT |
| `TransferFromQueue` | body | `boolean` | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. |
