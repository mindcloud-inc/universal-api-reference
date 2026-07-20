# Trigger Sync From ID or Slug with Hightouch

Triggers a sync run in Hightouch by ID or slug.

## Endpoint

- **Method:** `POST`
- **Path:** `/syncs/trigger`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [Trigger Sync From ID or Slug](https://api.hightouch.io/api/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `syncSlug` | body | `string` | no | Sync slug to trigger. |
| `syncId` | body | `string` | no | Sync ID to trigger. |
| `fullResync` | body | `boolean` | no | Whether to trigger a full resync. |
| `clearAndFill` | body | `boolean` | no | Whether to clear and fill when triggering the sync. |
| `resetCDC` | body | `boolean` | no | Whether to reset change data capture when triggering the sync. |
