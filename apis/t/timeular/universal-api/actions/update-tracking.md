# Timeular: Update Tracking

Updates the current tracking session in your Timeular workspace.

```
PUT https://connect.mindcloud.co/v1/universal/timeular/latest/actions/update-tracking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/update-tracking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeular/latest/actions/update-tracking', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activityId` | string | no |  |
| `note` | string | no |  |
| `startedAt` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activity": {
        "color": "string",
        "folderId": "string",
        "id": "string",
        "name": "Ava Chen"
      },
      "id": 1,
      "note": {
        "mentions": [
          {
            "folderId": "string",
            "id": 1,
            "key": "string",
            "label": "string",
            "scope": "string"
          }
        ],
        "tags": [
          {
            "folderId": "string",
            "id": 1,
            "key": "string",
            "label": "string",
            "scope": "string"
          }
        ],
        "text": "string"
      },
      "startedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activity.color` | string |  |
| `activity.folderId` | string |  |
| `activity.id` | string |  |
| `activity.name` | string |  |
| `id` | number |  |
| `note.mentions[].folderId` | string |  |
| `note.mentions[].id` | number |  |
| `note.mentions[].key` | string |  |
| `note.mentions[].label` | string |  |
| `note.mentions[].scope` | string |  |
| `note.tags[].folderId` | string |  |
| `note.tags[].id` | number |  |
| `note.tags[].key` | string |  |
| `note.tags[].label` | string |  |
| `note.tags[].scope` | string |  |
| `note.text` | string |  |
| `startedAt` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `PATCH /api/v4/tracking` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tracking.md) for the provider-specific parameters and requirements.

