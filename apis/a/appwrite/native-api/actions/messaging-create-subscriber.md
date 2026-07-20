# Create subscriber with Appwrite

Creates a new subscriber in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging/topics/{topicId}/subscribers`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create subscriber](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topicId` | path | `string` | yes | Topic ID. The topic ID to subscribe to. |
| `subscriberId` | body | `string` | yes | Subscriber ID. Choose a custom Subscriber ID or a new Subscriber ID. |
| `targetId` | body | `string` | yes | Target ID. The target ID to link to the specified Topic ID. |
