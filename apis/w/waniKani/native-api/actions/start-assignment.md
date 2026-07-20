# Start Assignment with WaniKani

Starts an assignment in WaniKani.

## Endpoint

- **Method:** `PUT`
- **Path:** `/assignments/[:id]/start`
- **Base URL:** `https://api.wanikani.com/v2`
- **Official documentation:** [Start Assignment](https://docs.api.wanikani.com/20170710/#start-an-assignment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Unique identifier of the assignment. |
