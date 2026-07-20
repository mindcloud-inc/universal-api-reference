# Delete Subscription with Pushbullet

Deletes an existing subscription from Pushbullet.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/subscriptions/:iden`
- **Base URL:** `https://api.pushbullet.com/v2`
- **Official documentation:** [Delete Subscription](https://docs.pushbullet.com/v8/#subscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `iden` | path | `string` | yes | Subscription identifier to delete. |
