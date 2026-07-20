# List Task Time Tracks with Amazing Marvin

Retrieves task time tracks from Amazing Marvin.

## Endpoint

- **Method:** `POST`
- **Path:** `/tracks`
- **Base URL:** `https://serv.amazingmarvin.com/api`
- **Official documentation:** [List Task Time Tracks](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#getting-time-track-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskIds[]` | body | `array<string>` | yes | List of up to 100 task IDs. |
