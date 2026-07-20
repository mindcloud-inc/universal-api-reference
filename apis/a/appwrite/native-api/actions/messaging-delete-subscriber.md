# Delete subscriber with Appwrite

Deletes the subscriber from your Appwrite project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/messaging/topics/{topicId}/subscribers/{subscriberId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Delete subscriber](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topicId` | path | `string` | yes | Topic ID. The topic ID subscribed to. |
| `subscriberId` | path | `string` | yes | Subscriber ID. |
