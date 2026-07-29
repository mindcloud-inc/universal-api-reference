# Insert Period with Rillion Prime Web Service

Insert an accounting period into the Prime register queue.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Period` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Period section. |
| `Period.Company` | body | `list<string>` | no | Company to which the period belongs |
| `Period.Year` | body | `number` | yes | Year (1-9999) |
| `Period.Period` | body | `number` | yes | Period (1-40) |
| `Period.Name` | body | `string` | yes | Name of period |
| `Period.StartDate` | body | `date` | yes | Start date for period |
| `Period.EndDate` | body | `date` | yes | End date for period |
| `Period.Closed` | body | `number` | no | Closed: 0=No; 1=Yes |
| `Period.Group1` | body | `string` | no | Free field of Type 1 |
| `Period.Group2` | body | `string` | no | Free field of Type 2 |
| `Period.Group3` | body | `string` | no | Free field of Type 3 |
| `Period.KeyType` | body | `number` | no | Is the company included in the primary key for the record: 0=No; 1=Yes |
| `Period.ExternalId` | body | `string` | no | — |
| `Period.ExternalSource` | body | `string` | no | — |
| `TransferFromQueue` | body | `boolean` | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. |
