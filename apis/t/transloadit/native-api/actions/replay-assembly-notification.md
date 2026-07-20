# Replay Assembly Notification with Transloadit

Replays an assembly notification in Transloadit.

## Endpoint

- **Method:** `POST`
- **Path:** `/assembly_notifications/:assemblyId/replay`
- **Base URL:** `https://api2.transloadit.com`
- **Official documentation:** [Replay Assembly Notification](https://transloadit.com/docs/api/assembly-notifications-assembly-id-replay-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assemblyId` | path | `string` | yes | The assembly ID whose notification should be replayed. |
| `params` | body | `string` | yes | JSON string required by Transloadit when replaying an assembly notification. |
