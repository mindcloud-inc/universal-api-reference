# Create List with DataMerge

Creates a new company or contact list in DataMerge.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/lists`
- **Base URL:** `https://api.datamerge.ai`
- **Official documentation:** [Create List](https://api.datamerge.ai/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | List name. |
| `object_type` | body | `string` | no | Type of objects stored in the list. |
