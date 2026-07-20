# List Task Discussions with Avaza

Retrieves task discussion messages from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/TaskDiscussion`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Task Discussions](https://api.avaza.com/#!/TaskDiscussion/TaskDiscussion_Get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TaskID` | query | `number` | yes | The TaskID of the Task to retrieve messages for |
| `startItem` | query | `number` | no | the ReponseID of the comment from which the page of results should start. |
