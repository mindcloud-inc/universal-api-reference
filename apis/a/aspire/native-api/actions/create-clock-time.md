# Create Clock Time with Aspire

## Endpoint

- **Method:** `POST`
- **Path:** `ClockTimes`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Clock Time](https://guide.youraspire.com/apidocs/clocktimes-5)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactID` | body | `list` | yes | — |
| `clockStartDateTime` | body | `date` | yes | — |
| `clockEndDateTime` | body | `date` | yes | — |
| `RouteID` | body | `list` | no | Either Route ID or Crew Leader Contact ID field is required |
| `crewLeaderContactID` | body | `list` | no | Either Route ID or Crew Leader Contact ID field is required |
| `BreakTime` | body | `number` | no | — |
| `ClockStartLat` | body | `number` | no | — |
| `ClockStartLong` | body | `number` | no | — |
| `ClockEndLat` | body | `number` | no | — |
| `ClockEndLong` | body | `number` | no | — |
