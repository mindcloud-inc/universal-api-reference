# Report Error with Honeybadger

Reports an application error to Honeybadger.

## Endpoint

- **Method:** `POST`
- **Path:** `/notices`
- **Base URL:** `https://api.honeybadger.io/v1`
- **Official documentation:** [Report Error](https://docs.honeybadger.io/api/reporting-exceptions/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `notifier.name` | body | `string` | no | Name of the notifier sending the Honeybadger error report. |
| `notifier.url` | body | `string` | no | URL for the notifier package or integration. |
| `notifier.version` | body | `string` | no | Version of the notifier package or integration. |
| `error.class` | body | `string` | yes | Error class or exception type. |
| `error.message` | body | `string` | yes | Human-readable error message. |
| `error.backtrace[]` | body | `array<object>` | yes | Ruby-style backtrace frames for grouping and error inspection. |
