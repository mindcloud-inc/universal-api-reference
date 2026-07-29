# Insert Holiday with Rillion Prime Web Service

Insert a holiday calendar entry into the Prime register queue.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Holiday` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Holiday section. |
| `Holiday.Company` | body | `list<string>` | no | Company for the holiday |
| `Holiday.Holiday` | body | `date` | yes | Holiday |
| `Holiday.ExternalId` | body | `string` | no | — |
| `Holiday.ExternalSource` | body | `string` | no | — |
| `TransferFromQueue` | body | `boolean` | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. |
