# Report Check-in Details with Honeybadger

Reports check-in details to Honeybadger by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/check_in/:checkInId`
- **Base URL:** `https://api.honeybadger.io/v1`
- **Official documentation:** [Report Check-in Details](https://docs.honeybadger.io/api/reporting-check-ins/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checkInId` | path | `string` | yes | The case-sensitive check-in endpoint ID from Honeybadger. |
| `check_in.status` | body | `string` | no | Check-in result status: success or error. |
| `check_in.duration` | body | `number` | no | Execution duration in milliseconds. |
| `check_in.stdout` | body | `string` | no | Captured standard output. |
| `check_in.stderr` | body | `string` | no | Captured standard error. |
| `check_in.exit_code` | body | `number` | no | Process exit code. |
