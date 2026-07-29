# Insert Currency with Rillion Prime Web Service

Insert a currency exchange rate into the Prime register queue.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Currency` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Currency section. |
| `Currency.BaseCurrency` | body | `string` | yes | Currency for accounting purpose |
| `Currency.Currency` | body | `string` | yes | Currency |
| `Currency.FromAccountCodingDate` | body | `date` | no | Date from which exchange rate to be used |
| `Currency.BuyingRate` | body | `number` | yes | Buying rate |
| `Currency.Group1` | body | `string` | no | Free field of Type 1 |
| `Currency.Group2` | body | `string` | no | Free field of Type 2 |
| `Currency.Group3` | body | `string` | no | Free field of Type 3 |
| `Currency.Company` | body | `list<string>` | no | Company for the currency |
| `Currency.KeyType` | body | `number` | no | Is the company included in the primary key for the record: 0=No; 1=Yes |
| `Currency.ExternalId` | body | `string` | no | — |
| `Currency.ExternalSource` | body | `string` | no | — |
| `TransferFromQueue` | body | `boolean` | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. |
