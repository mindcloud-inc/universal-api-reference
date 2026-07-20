# Update Sync with Hightouch

Updates an existing sync in Hightouch.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/syncs/{syncId}`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [Update Sync](https://api.hightouch.io/api/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `syncId` | path | `number` | yes | The sync ID. |
| `configuration` | body | `object` | no | Sync configuration object. |
| `schedule` | body | `object` | no | Sync schedule configuration object. |
| `disabled` | body | `boolean` | no | Whether the sync is disabled. |
