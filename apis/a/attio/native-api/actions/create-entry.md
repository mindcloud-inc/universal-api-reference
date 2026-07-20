# Create Entry with Attio

Creates a list entry in Attio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/lists/:list/entries`
- **Base URL:** `https://api.attio.com`
- **Official documentation:** [Create Entry](https://docs.attio.com/rest-api/endpoint-reference/entries/create-an-entry-add-record-to-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list` | path | `string` | yes | The UUID or slug identifying the list. |
| `parentObject` | body | `string<string>` | yes | The parent object slug or UUID for the record being added to the list. |
| `parentRecordId` | body | `string` | yes | The record ID to add to the list. |
| `entryValues` | body | `object` | no | Optional list entry values keyed by Attio attribute slug or attribute ID. |
