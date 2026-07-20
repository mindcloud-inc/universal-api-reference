# Update Record with Attio

Updates a record in Attio.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/objects/:object/records/:record_id`
- **Base URL:** `https://api.attio.com`
- **Official documentation:** [Update Record](https://docs.attio.com/rest-api/endpoint-reference/records/update-a-record-overwrite-multiselect-values)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `object` | path | `string` | yes | The Attio object slug or UUID containing the record. |
| `record_id` | path | `string` | yes | The Attio record UUID to update. |
| `values` | body | `object` | yes | Record values keyed by Attio attribute slug or attribute ID. This overwrite endpoint replaces current multiselect values. |
