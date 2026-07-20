# Create Batch with Print.one Postcards

Creates a new batch in Print.one Postcards.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/batches`
- **Base URL:** `https://api.print.one`
- **Official documentation:** [Create Batch](https://api.print.one/docs/v2#operation/Batch/createBatch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the batch |
| `templateId` | body | `string` | yes | Template ID every order in the batch will use |
| `finish` | body | `string` | yes | Finish every order in the batch will use |
| `ready` | body | `boolean` | yes | When true, send the batch as soon as requirements are met |
| `requiredCount` | body | `number` | yes | Minimum number of orders required before the batch is sent |
