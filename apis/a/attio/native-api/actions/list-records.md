# List Records with Attio

Retrieves records from Attio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/objects/:object/records/query`
- **Base URL:** `https://api.attio.com`
- **Official documentation:** [List Records](https://docs.attio.com/rest-api/endpoint-reference/records/list-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `object` | path | `string` | yes | The Attio object slug or UUID whose records you want to query. |
| `filter` | body | `object` | no | Records query filter object for the selected Attio object. |
| `sorts[]` | body | `array<object>` | no | Sort definitions array for the records query body. |
| `limit` | body | `number` | no | Maximum number of records to return. |
| `offset` | body | `number` | no | Number of matching records to skip before returning results. |
