# Create Queue with Request Tracker (RT)

Creates a new queue in Request Tracker.

## Endpoint

- **Method:** `POST`
- **Path:** `queue`
- **Base URL:** `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`
- **Official documentation:** [Create Queue](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Queues)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Description` | body | `string` | no | Queue description. |
| `Name` | body | `string` | yes | Queue name. |
