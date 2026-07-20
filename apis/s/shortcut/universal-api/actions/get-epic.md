# Shortcut: Get Epic



```
GET https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/get-epic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shortcut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/get-epic?connectionId=$CONNECTION_ID&epicPublicId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "epicPublicId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/get-epic?${params}`, {
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
| `epicPublicId` | number | yes | The public ID of the epic. |

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

Through the native Shortcut API, this operation is `GET /epics/:epicPublicId` (base URL `https://api.app.shortcut.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-epic.md) for the provider-specific parameters and requirements.

