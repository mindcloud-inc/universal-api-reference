# Create Schedule with Cronfree Time Scheduler

Creates a new schedule in Cronfree Time Scheduler.

## Endpoint

- **Method:** `POST`
- **Path:** `/schedule`
- **Base URL:** `https://login.cronfree.com/zapier`
- **Official documentation:** [Create Schedule](https://docs.cronfree.com/api#subscribe-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hookUrl` | body | `string` | yes | The URL that Cronfree will POST to at the scheduled interval. |
| `wdays[]` | body | `array<string>` | yes | — |
| `months[]` | body | `array<string>` | yes | — |
| `mdays[]` | body | `array<string>` | yes | — |
| `hours[]` | body | `array<string>` | yes | — |
| `minutes[]` | body | `array<string>` | yes | — |
| `timezone` | body | `string` | yes | — |
