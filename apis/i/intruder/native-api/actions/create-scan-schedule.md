# Create Scan Schedule with Intruder

## Endpoint

- **Method:** `POST`
- **Path:** `/scans/schedules/`
- **Base URL:** `https://api.intruder.io/v1`
- **Official documentation:** [Create Scan Schedule](https://developers.intruder.io/reference/scans_schedules_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Schedule name. |
| `first_scan_time` | body | `date` | no | First scan time in the future on the hour. |
| `scan_frequency` | body | `string` | yes | How often the schedule runs. |
| `tags[]` | body | `array<string>` | no | Tag names to include in the scan. |
| `targets[]` | body | `array<number>` | no | Target IDs to include in the scan. |
| `throttled` | body | `boolean` | no | Run the schedule in throttled mode. |
| `web_ports_only` | body | `boolean` | no | Limit scans to web ports only. |
| `upload_to_drata` | body | `boolean` | no | Upload findings to Drata. |
| `upload_to_vanta` | body | `boolean` | no | Upload findings to Vanta. |
