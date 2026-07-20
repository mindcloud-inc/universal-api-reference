# Assert Record with Attio

Creates or updates a record in Attio by matching attribute.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/objects/:object/records`
- **Base URL:** `https://api.attio.com`
- **Official documentation:** [Assert Record](https://docs.attio.com/rest-api/endpoint-reference/records/assert-a-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `object` | path | `string` | yes | The Attio object slug or UUID containing the record. |
| `matching_attribute` | query | `string` | yes | The unique Attio attribute slug or UUID used to match an existing record before create-or-update. |
| `values` | body | `object` | yes | Record values keyed by Attio attribute slug or attribute ID. |
