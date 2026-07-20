# Pitchbox: List Tasks



```
GET https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pitchbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-tasks?connectionId=$CONNECTION_ID&project.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-tasks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project.id` | string | yes | Filter tasks by Pitchbox project identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedTo": {
        "displayName": "Ava Chen"
      },
      "autocompleteOnCommunication": true,
      "autocompleteOnMilestone": true,
      "campaign": {
        "id": 1,
        "name": "Ava Chen",
        "status": "string"
      },
      "completedAt": "2026-05-07T12:00:00.000Z",
      "completedBy": {
        "displayName": "Ava Chen"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "opportunity": {
        "id": 1,
        "milestone": "string",
        "name": "Ava Chen",
        "url": "https://example.com"
      },
      "project": {
        "id": 1,
        "name": "Ava Chen"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedTo.displayName` | string |  |
| `autocompleteOnCommunication` | boolean |  |
| `autocompleteOnMilestone` | boolean |  |
| `campaign.id` | number |  |
| `campaign.name` | string |  |
| `campaign.status` | string |  |
| `completedAt` | date |  |
| `completedBy.displayName` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `dueDate` | date |  |
| `id` | number |  |
| `name` | string |  |
| `opportunity.id` | number |  |
| `opportunity.milestone` | string |  |
| `opportunity.name` | string |  |
| `opportunity.url` | string |  |
| `project.id` | number |  |
| `project.name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Pitchbox API, this operation is `GET /api/tasks` (base URL `https://apiv2.pitchbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

