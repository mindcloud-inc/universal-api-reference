# Update Queue with Request Tracker (RT)

Updates an existing queue in Request Tracker.

## Endpoint

- **Method:** `PUT`
- **Path:** `queue/:queueId`
- **Base URL:** `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`
- **Official documentation:** [Update Queue](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Queues)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Description` | body | `string` | no | Updated queue description. |
| `Disabled` | body | `boolean` | no | Set to true to disable the queue. |
| `Name` | body | `string` | no | Updated queue name. |
| `queueId` | path | `string` | yes | The RT queue ID or queue name. |
