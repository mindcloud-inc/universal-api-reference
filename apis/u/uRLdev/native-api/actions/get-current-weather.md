# Get Current Weather with URL.dev

Retrieves current weather for coordinates from URL.dev.

## Endpoint

- **Method:** `GET`
- **Path:** `/current/`
- **Base URL:** `https://v-20260317--open-meteo--superuser.su.dev`
- **Official documentation:** [Get Current Weather](https://superuser.app/org/superuser/toolkits/open-meteo/v-20260317/functions/current.js?method=GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | query | `number` | yes | Latitude coordinate for the current weather lookup. |
| `longitude` | query | `number` | yes | Longitude coordinate for the current weather lookup. |
