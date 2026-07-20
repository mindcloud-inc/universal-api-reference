# Shortcut: List Objective Epics



```
GET https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/list-objective-epics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shortcut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/list-objective-epics?connectionId=$CONNECTION_ID&objectivePublicId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "objectivePublicId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/list-objective-epics?${params}`, {
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
| `objectivePublicId` | number | yes | The public ID of the objective. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "entityType": "string",
      "epicStateId": 1,
      "groupId": "string",
      "id": 1,
      "milestoneId": 1,
      "name": "Ava Chen",
      "requestedById": "string",
      "state": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `createdAt` | date |  |
| `description` | string |  |
| `entityType` | string |  |
| `epicStateId` | number |  |
| `groupId` | string |  |
| `id` | number |  |
| `milestoneId` | number |  |
| `name` | string |  |
| `requestedById` | string |  |
| `state` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Shortcut API, this operation is `GET /objectives/:objectivePublicId/epics` (base URL `https://api.app.shortcut.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-objective-epics.md) for the provider-specific parameters and requirements.

