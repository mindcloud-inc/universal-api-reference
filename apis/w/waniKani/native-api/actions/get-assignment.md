# Get Assignment with WaniKani

Retrieves an assignment from WaniKani.

## Endpoint

- **Method:** `GET`
- **Path:** `/assignments/[:id]`
- **Base URL:** `https://api.wanikani.com/v2`
- **Official documentation:** [Get Assignment](https://docs.api.wanikani.com/20170710/#get-a-specific-assignment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Unique identifier of the assignment. |
