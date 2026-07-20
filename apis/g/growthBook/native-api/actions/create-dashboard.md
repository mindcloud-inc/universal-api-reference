# Create a single dashboard with GrowthBook

Creates a new dashboard in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/dashboards`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a single dashboard](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The display name of the Dashboard |
| `editLevel` | body | `string` | yes | Dashboards that are "published" are editable by organization members with appropriate permissions |
| `shareLevel` | body | `string` | yes | General Dashboards only. Dashboards that are "published" are viewable by organization members with appropriate permissions |
| `enableAutoUpdates` | body | `boolean` | yes | If enabled for a General Dashboard, also requires an updateSchedule |
| `updateSchedule` | body | `object` | no | — |
| `experimentId` | body | `string` | no | The parent experiment for an Experiment Dashboard, or undefined for a general dashboard |
| `projects` | body | `list<string>` | no | General Dashboards only, Experiment Dashboards use the experiment's projects |
| `blocks[]` | body | `array<object>` | yes | — |
