# Track Task Time with Amazing Marvin

Starts or stops task time tracking in Amazing Marvin.

## Endpoint

- **Method:** `POST`
- **Path:** `/track`
- **Base URL:** `https://serv.amazingmarvin.com/api`
- **Official documentation:** [Track Task Time](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#startstop-time-tracking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | body | `string` | yes | Task ID to track. |
| `action` | body | `string` | yes | START or STOP. |
