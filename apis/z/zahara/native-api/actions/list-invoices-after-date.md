# List Invoices After Date with Zahara

Retrieves invoices from Zahara after a specific date.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/{businessUnitApiKey}/Invoice/After/{{date}}/{{skip}}/{{take}}`
- **Base URL:** `https://api.myzahara.net`
- **Official documentation:** [List Invoices After Date](https://ask.zaharasoftware.com/api-docs/get-invoices-after-date-with-skip-and-take)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | path | `string` | yes | Return invoices created after this date. |
| `skip` | path | `number` | yes | Number of records to skip. |
| `take` | path | `number` | yes | Number of records to return. |
