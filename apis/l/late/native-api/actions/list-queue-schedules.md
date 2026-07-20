# List Queue Schedules with Late

## Endpoint

- **Method:** `GET`
- **Path:** `/queue/slots`
- **Base URL:** `https://zernio.com/api/v1`
- **Official documentation:** [List Queue Schedules](https://docs.zernio.com/queue/list-schedules)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `profileId` | query | `string` | yes |
| `queueId` | query | `string` | no |
| `all` | query | `boolean` | no |
