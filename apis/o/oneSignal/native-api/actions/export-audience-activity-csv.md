# Export Audience Activity CSV with OneSignal

Exports audience activity as CSV from OneSignal.

## Endpoint

- **Method:** `POST`
- **Path:** `/notifications/:message_id/export_events`
- **Base URL:** `https://api.onesignal.com`
- **Official documentation:** [Export Audience Activity CSV](https://documentation.onesignal.com/reference/export-csv-of-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_id` | path | `string` | yes | The identifier of the message in UUID v4 format. |
