# Insert Object with Rillion Prime Web Service

Insert an accounting object (coding dimension value) into the Prime register queue.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Object` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Object section. |
| `Object.Company` | body | `list<string>` | no | Company to which object belongs |
| `Object.ObjectTypeNo` | body | `number` | yes | Object type number (1-8) |
| `Object.Object` | body | `string` | yes | Object |
| `Object.Name` | body | `string` | yes | Object name |
| `Object.ValidFrom` | body | `date` | no | Valid from |
| `Object.ValidTo` | body | `date` | no | Valid until |
| `Object.VatDeduction` | body | `number` | no | Percentage liable for VAT |
| `Object.DefaultObject1` | body | `string` | no | Which object of Type 1 is to be set automatically |
| `Object.DefaultObject2` | body | `string` | no | Which object of Type 2 is to be set automatically |
| `Object.DefaultObject3` | body | `string` | no | Which object of Type 3 is to be set automatically |
| `Object.DefaultObject4` | body | `string` | no | Which object of Type 4 is to be set automatically |
| `Object.DefaultObject5` | body | `string` | no | Which object of Type 5 is to be set automatically |
| `Object.DefaultObject6` | body | `string` | no | Which object of Type 6 is to be set automatically |
| `Object.DefaultObject7` | body | `string` | no | Which object of Type 7 is to be set automatically |
| `Object.DefaultObject8` | body | `string` | no | Which object of Type 8 is to be set automatically |
| `Object.Group1` | body | `string` | no | Free field of Type 1 |
| `Object.Group2` | body | `string` | no | Free field of Type 2 |
| `Object.Group3` | body | `string` | no | Free field of Type 3 |
| `Object.Remove` | body | `number` | no | Should record be removed: 0=No; 1=Yes |
| `Object.KeyType` | body | `number` | no | Is the company included in the primary key for the record: 0=No; 1=Yes |
| `Object.ExternalId` | body | `string` | no | — |
| `Object.ExternalSource` | body | `string` | no | — |
| `TransferFromQueue` | body | `boolean` | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. |
