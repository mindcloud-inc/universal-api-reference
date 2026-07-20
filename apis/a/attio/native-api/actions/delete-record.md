# Delete Record with Attio

Deletes a record from Attio.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/objects/:object/records/:record_id`
- **Base URL:** `https://api.attio.com`
- **Official documentation:** [Delete Record](https://docs.attio.com/rest-api/endpoint-reference/records/delete-a-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `object` | path | `string` | yes | The Attio object slug or UUID containing the record. |
| `record_id` | path | `string` | yes | The Attio record UUID to delete. |
