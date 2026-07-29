# Insert Account with Rillion Prime Web Service

Insert a general ledger account into the Prime register queue.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Account` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Account section. |
| `Account.Company` | body | `list<string>` | no | Company that account is used for |
| `Account.Account` | body | `string` | yes | Account |
| `Account.Name` | body | `string` | no | Account name |
| `Account.ValidTo` | body | `date` | no | Valid until |
| `Account.VatCode` | body | `string` | no | VAT code |
| `Account.AllocationsAccount` | body | `string` | no | Default allocations account for the account |
| `Account.IsAllocationsAccount` | body | `number` | no | Can account be used as an allocations account: 0=No; 1=Yes |
| `Account.VatCodeMandatory` | body | `number` | no | VatCode is mandatory when using account: 0=No; 1=Yes |
| `Account.NoteMandatory` | body | `number` | no | Note is mandatory when using account: 0=No; 1=Yes |
| `Account.UseObject1` | body | `number` | no | Is object of Type 1 to be registered: 0=Never; 1=Optional; 2=Mandatory |
| `Account.UseObject2` | body | `number` | no | Is object of Type 2 to be registered: 0=Never; 1=Optional; 2=Mandatory |
| `Account.UseObject3` | body | `number` | no | Is object of Type 3 to be registered: 0=Never; 1=Optional; 2=Mandatory |
| `Account.UseObject4` | body | `number` | no | Is object of Type 4 to be registered: 0=Never; 1=Optional; 2=Mandatory |
| `Account.UseObject5` | body | `number` | no | Is object of Type 5 to be registered: 0=Never; 1=Optional; 2=Mandatory |
| `Account.UseObject6` | body | `number` | no | Is object of Type 6 to be registered: 0=Never; 1=Optional; 2=Mandatory |
| `Account.UseObject7` | body | `number` | no | Is object of Type 7 to be registered: 0=Never; 1=Optional; 2=Mandatory |
| `Account.UseObject8` | body | `number` | no | Is object of Type 8 to be registered: 0=Never; 1=Optional; 2=Mandatory |
| `Account.DefaultObject1` | body | `string` | no | Which object of Type 1 is to be set automatically |
| `Account.DefaultObject2` | body | `string` | no | Which object of Type 2 is to be set automatically |
| `Account.DefaultObject3` | body | `string` | no | Which object of Type 3 is to be set automatically |
| `Account.DefaultObject4` | body | `string` | no | Which object of Type 4 is to be set automatically |
| `Account.DefaultObject5` | body | `string` | no | Which object of Type 5 is to be set automatically |
| `Account.DefaultObject6` | body | `string` | no | Which object of Type 6 is to be set automatically |
| `Account.DefaultObject7` | body | `string` | no | Which object of Type 7 is to be set automatically |
| `Account.DefaultObject8` | body | `string` | no | Which object of Type 8 is to be set automatically |
| `Account.Group1` | body | `string` | no | Free field of Type 1 |
| `Account.Group2` | body | `string` | no | Free field of Type 2 |
| `Account.Group3` | body | `string` | no | Free field of Type 3 |
| `Account.Remove` | body | `number` | no | — |
| `Account.KeyType` | body | `number` | yes | Is the company included in the primary key for the record: 0=No; 1=Yes |
| `Account.ExternalId` | body | `string` | no | — |
| `Account.ExternalSource` | body | `string` | no | — |
| `TransferFromQueue` | body | `boolean` | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. |
