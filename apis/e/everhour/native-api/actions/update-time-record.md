# Update Time Record with Everhour

Updates an existing time record in Everhour.

## Endpoint

- **Method:** `PUT`
- **Path:** `/time/:timeId`
- **Base URL:** `https://api.everhour.com`
- **Official documentation:** [Update Time Record](https://everhour.docs.apiary.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `timeId` | path | `number` | yes | Everhour time record ID. |
| `time` | body | `number` | yes | Duration in seconds. |
| `date` | body | `string` | yes | Record date in YYYY-MM-DD format. |
| `task` | body | `string` | no | Optional task ID. |
| `user` | body | `number` | no | Optional user ID. |
| `comment` | body | `string` | no | Optional time record note. |
