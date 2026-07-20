# Create Collection with vPlan

## Endpoint

- **Method:** `POST`
- **Path:** `/collection`
- **Base URL:** `https://api.vplan.com/v1`
- **Official documentation:** [Create Collection](https://docs.api.vplan.com/collection.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | body | `string` | yes | Board identifier for the new collection. |
| `name` | body | `string` | yes | Collection name. |
