# List Queue Discussions with Tender Support

Retrieves discussions from a Tender Support queue.

## Endpoint

- **Method:** `GET`
- **Path:** `/queues/:queueId/discussions`
- **Base URL:** `https://api.tenderapp.com/help`
- **Official documentation:** [List Queue Discussions](https://help.tenderapp.com/kb/api/queues)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queueId` | path | `string` | yes | The queue ID or the special value 'mine'. |
