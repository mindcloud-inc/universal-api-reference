# Delete File with Slack

Deletes an existing file from Slack.

## Endpoint

- **Method:** `POST`
- **Path:** `files.delete`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Delete File](https://docs.slack.dev/reference/methods/files.delete/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | body | `list<string>` | no | Channel containing the file to be deleted. |
| `file` | body | `list<string>` | no | ID of file to delete. |
