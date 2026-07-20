# Create Sync with Hightouch

Creates a new sync in Hightouch.

## Endpoint

- **Method:** `POST`
- **Path:** `/syncs`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [Create Sync](https://api.hightouch.io/api/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | body | `string` | yes | The sync slug. |
| `configuration` | body | `object` | yes | Sync configuration object. |
| `destinationId` | body | `number` | yes | Destination ID connected to the sync. |
| `modelId` | body | `number` | yes | Model ID connected to the sync. |
| `schedule` | body | `object` | yes | Sync schedule configuration object. |
| `disabled` | body | `boolean` | yes | Whether the sync is disabled. |
