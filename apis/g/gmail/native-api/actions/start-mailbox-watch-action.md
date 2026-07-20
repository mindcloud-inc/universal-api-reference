# Start Mailbox Watch (Action) with Google Mail

Sets up or updates a Gmail mailbox watch.

## Endpoint

- **Method:** `POST`
- **Path:** `/watch`
- **Base URL:** `https://gmail.googleapis.com/gmail/v1/users/:userId`
- **Official documentation:** [Start Mailbox Watch (Action)](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users/watch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topicName` | body | `string` | yes | Fully-qualified Pub/Sub topic name (`projects/{project}/topics/{topic}`). |
| `labelFilterBehavior` | body | `string` | no | How labels should be applied when filtering watch notifications (`include` or `exclude`). |
