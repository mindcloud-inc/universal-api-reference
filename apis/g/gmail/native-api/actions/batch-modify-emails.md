# Batch Modify Emails with Google Mail

Updates labels on multiple Gmail messages.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/batchModify`
- **Base URL:** `https://gmail.googleapis.com/gmail/v1/users/:userId`
- **Official documentation:** [Batch Modify Emails](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.messages/batchModify)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | yes | The IDs of the messages to modify. Gmail accepts at most 1,000 IDs per request. |
| `addLabelIds` | body | `list<string>` | no | A list of label IDs to add to the messages. Send multiple values as a array. |
| `removeLabelIds` | body | `list<string>` | no | A list of label IDs to remove from the messages. Send multiple values as a array. |
