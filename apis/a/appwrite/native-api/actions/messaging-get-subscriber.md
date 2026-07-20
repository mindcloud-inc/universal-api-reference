# Get subscriber with Appwrite

Retrieves the subscriber from your Appwrite project.

## Endpoint

- **Method:** `GET`
- **Path:** `/messaging/topics/{topicId}/subscribers/{subscriberId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get subscriber](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topicId` | path | `string` | yes | Topic ID. The topic ID subscribed to. |
| `subscriberId` | path | `string` | yes | Subscriber ID. |
