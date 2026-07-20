# Assert List Entry by Parent with Attio

Creates or updates a list entry in Attio by parent record.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/lists/:list/entries`
- **Base URL:** `https://api.attio.com`
- **Official documentation:** [Assert List Entry by Parent](https://docs.attio.com/rest-api/endpoint-reference/entries/assert-a-list-entry-by-parent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list` | path | `string` | yes | The UUID or slug identifying the list. |
| `parentObject` | body | `string<string>` | yes | The parent object slug or UUID used to identify the list entry by parent record. |
| `parentRecordId` | body | `string` | yes | The record ID used to identify the list entry by parent record. |
| `entryValues` | body | `object` | no | Optional list entry values keyed by Attio attribute slug or attribute ID. |
