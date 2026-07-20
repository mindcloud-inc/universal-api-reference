# Reply to Online Review with GatherUp

Creates a reply to an online review in GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/online-review/reply`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [Reply to Online Review](https://app.gatherup.com/api/doc/online-review/reply)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reviewId` | body | `number` | yes | Review ID |
| `content` | body | `string` | yes | The content of the comment. |
