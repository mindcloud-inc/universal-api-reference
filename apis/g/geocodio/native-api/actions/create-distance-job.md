# Create Distance Job with Geocodio

Creates an asynchronous distance job in Geocodio.

## Endpoint

- **Method:** `POST`
- **Path:** `/distance-jobs`
- **Base URL:** `https://api.geocod.io/v1.12`
- **Official documentation:** [Create Distance Job](https://www.geocod.io/docs/#distance-jobs-async)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | A name for the distance matrix job. |
| `origins[]` | body | `array<string>` | yes | Origin list ID or array of coordinates/addresses. |
| `destinations[]` | body | `array<string>` | yes | Destination list ID or array of coordinates/addresses. |
| `distance_mode` | body | `string` | no | Distance calculation mode: driving or straightline. Accepted values: `0`, `1`. |
| `callback_url` | body | `string` | no | Optional webhook URL to call when the job completes. |
