# Create topic with Appwrite

Creates a new topic in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging/topics`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create topic](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscribe` | body | `string` | no | An array of role strings with subscribe permission. By default all users are granted with any subscribe permission. [learn more about roles](https://appwrite.io/docs/permissions#permission-roles). Maximum of 100 roles are allowed, each 64 characters long. |
| `topicId` | body | `string` | yes | Topic ID. Choose a custom Topic ID or a new Topic ID. |
| `name` | body | `string` | yes | Topic Name. |
| `subscribe[]` | body | `array<string>` | no | An array of role strings with subscribe permission. By default all users are granted with any subscribe permission. [learn more about roles](https://appwrite.io/docs/permissions#permission-roles). Maximum of 100 roles are allowed, each 64 characters long. |
