# Get Job with Workiz

Retrieves a job from Workiz by UUID.

## Endpoint

- **Method:** `GET`
- **Path:** `/job/get/:UUID/`
- **Base URL:** `https://api.workiz.com/api/v1/{apiKey}`
- **Official documentation:** [Get Job](https://developer.workiz.com/#/Jobs/getJob)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UUID` | path | `string` | yes | The job's UUID. |
