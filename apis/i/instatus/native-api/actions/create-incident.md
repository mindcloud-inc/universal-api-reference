# Create Incident with Instatus

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/:page_id/incidents`
- **Base URL:** `https://api.instatus.com`
- **Official documentation:** [Create Incident](https://instatus.com/help/api/incidents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | no | Initial incident message. |
| `name` | body | `string` | no | Incident name. |
| `page_id` | path | `string` | yes | Instatus status page ID. |
| `started` | body | `string` | no | Incident start time. |
| `status` | body | `string` | no | Incident status, such as INVESTIGATING, IDENTIFIED, MONITORING, or RESOLVED. |
| `components[]` | body | `array<string>` | no | Affected component IDs. Send multiple values as a array. |
| `notify` | body | `boolean` | no | Whether to notify subscribers. |
| `shouldPublish` | body | `boolean` | no | Set false to create an unpublished incident. |
