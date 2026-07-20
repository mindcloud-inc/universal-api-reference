# Run Website Traffic Checker with Botster

Creates a Botster website traffic estimate job.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/website-traffic-checker`
- **Base URL:** `https://botster.io/api/v2`
- **Official documentation:** [Run Website Traffic Checker](https://botster.io/bots/website-traffic-checker)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Websites to check. |
| `period` | body | `string` | yes | Display period such as daily or weekly. |
| `timeframe` | body | `string` | yes | Timeframe for traffic history. |
