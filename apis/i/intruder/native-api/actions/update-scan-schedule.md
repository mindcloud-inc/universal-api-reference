# Update Scan Schedule with Intruder

## Endpoint

- **Method:** `PATCH`
- **Path:** `/scans/schedules/:id/`
- **Base URL:** `https://api.intruder.io/v1`
- **Official documentation:** [Update Scan Schedule](https://developers.intruder.io/reference/scans_schedules_partial_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Scan schedule ID. |
| `name` | body | `string` | no | Schedule name. |
| `first_scan_time` | body | `date` | no | First scan time in the future on the hour. |
| `scan_frequency` | body | `string` | no | How often the schedule runs. |
| `tags[]` | body | `array<string>` | no | Tag names to include in the scan. |
| `targets[]` | body | `array<number>` | no | Target IDs to include in the scan. |
| `throttled` | body | `boolean` | no | Run the schedule in throttled mode. |
| `web_ports_only` | body | `boolean` | no | Limit scans to web ports only. |
| `upload_to_drata` | body | `boolean` | no | Upload findings to Drata. |
| `upload_to_vanta` | body | `boolean` | no | Upload findings to Vanta. |
