# Add Time with Everhour

Creates a new time record in Everhour.

## Endpoint

- **Method:** `POST`
- **Path:** `/time`
- **Base URL:** `https://api.everhour.com`
- **Official documentation:** [Add Time](https://everhour.docs.apiary.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `time` | body | `number` | yes | Duration in seconds. |
| `date` | body | `string` | yes | Record date in YYYY-MM-DD format. |
| `task` | body | `string` | no | Optional task ID. |
| `user` | body | `number` | no | Optional user ID. |
| `comment` | body | `string` | no | Optional time record note. |
