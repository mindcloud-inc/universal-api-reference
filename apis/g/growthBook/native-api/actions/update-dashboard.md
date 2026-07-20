# Update a single dashboard with GrowthBook

Updates an existing dashboard in GrowthBook.

## Endpoint

- **Method:** `PUT`
- **Path:** `/dashboards/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Update a single dashboard](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `title` | body | `string` | no | The display name of the Dashboard |
| `editLevel` | body | `string` | no | Dashboards that are "published" are editable by organization members with appropriate permissions |
| `shareLevel` | body | `string` | no | General Dashboards only. Dashboards that are "published" are viewable by organization members with appropriate permissions |
| `enableAutoUpdates` | body | `boolean` | no | If enabled for a General Dashboard, also requires an updateSchedule |
| `updateSchedule` | body | `object` | no | — |
| `projects` | body | `list<string>` | no | General Dashboards only, Experiment Dashboards use the experiment's projects |
| `blocks[]` | body | `array<object>` | no | — |
