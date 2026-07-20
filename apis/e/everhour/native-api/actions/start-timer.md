# Start Timer with Everhour

Starts a timer in Everhour.

## Endpoint

- **Method:** `POST`
- **Path:** `/timers`
- **Base URL:** `https://api.everhour.com`
- **Official documentation:** [Start Timer](https://everhour.docs.apiary.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task` | body | `string` | yes | Task ID to start the timer on. |
| `userDate` | body | `string` | no | Date to attribute the timer to in YYYY-MM-DD format. |
| `comment` | body | `string` | no | Optional timer note. |
