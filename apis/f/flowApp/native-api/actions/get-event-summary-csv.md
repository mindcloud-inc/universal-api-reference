# Get Event Summary CSV with Flow App

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/events/sessions/csv/summary/:sessionToken`
- **Base URL:** `https://prod.flowapp.com/api/v1`
- **Official documentation:** [Get Event Summary CSV](https://support.flowapp.com/support/solutions/articles/12000076814-flow-api-0-0-4)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionToken` | path | `string` | yes | The event session token for the compiled summary CSV report. |
