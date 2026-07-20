# Trigger Sync with Hightouch

Triggers a sync run in Hightouch.

## Endpoint

- **Method:** `POST`
- **Path:** `/syncs/{syncId}/trigger`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [Trigger Sync](https://api.hightouch.io/api/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `syncId` | path | `string` | yes | The sync ID. |
| `clearAndFill` | body | `boolean` | no | Whether to clear and fill when triggering the sync. |
| `resetCDC` | body | `boolean` | no | Whether to reset change data capture when triggering the sync. |
| `fullResync` | body | `boolean` | no | Whether to trigger a full resync. |
