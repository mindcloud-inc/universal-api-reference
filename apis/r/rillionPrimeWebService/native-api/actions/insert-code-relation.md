# Insert Code Relation with Rillion Prime Web Service

Insert a coding relation into the Prime register queue.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CodeRelation` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, CodeRelation section. |
| `CodeRelation.Company` | body | `list<string>` | no | Company that rule is linked to |
| `CodeRelation.SelectAccount` | body | `string` | no | Filter by account |
| `CodeRelation.SelectObject1` | body | `string` | no | Filter by object of Type 1 |
| `CodeRelation.SelectObject2` | body | `string` | no | Filter by object of Type 2 |
| `CodeRelation.SelectObject3` | body | `string` | no | Filter by object of Type 3 |
| `CodeRelation.SelectObject4` | body | `string` | no | Filter by object of Type 4 |
| `CodeRelation.SelectObject5` | body | `string` | no | Filter by object of Type 5 |
| `CodeRelation.SelectObject6` | body | `string` | no | Filter by object of Type 6 |
| `CodeRelation.SelectObject7` | body | `string` | no | Filter by object of Type 7 |
| `CodeRelation.SelectObject8` | body | `string` | no | Filter by vat code |
| `CodeRelation.FromDate` | body | `date` | no | Rule active from this date |
| `CodeRelation.ToDate` | body | `date` | no | Rule active until this date |
| `CodeRelation.Blocked` | body | `number` | no | Does the rule refer to a blocked relation: 0=No; 1=Yes |
| `CodeRelation.BlockedMessage` | body | `string` | no | Error text if Blocked=1 |
| `CodeRelation.ExternalId` | body | `string` | no | — |
| `CodeRelation.ExternalSource` | body | `string` | no | — |
| `CodeRelation.SelectVatCode` | body | `string` | yes | Filter by object of Type 9 |
| `CodeRelation.UseAsFilter` | body | `boolean` | no | Allocation setting |
| `TransferFromQueue` | body | `boolean` | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. |
