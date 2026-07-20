# Teamgate: Get Activity

Retrieves an activity from Teamgate.

```
GET https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/get-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamgate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/get-activity?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/get-activity?${params}`, {
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
| `eventId` | string | yes | Unique key of the activity. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allDay": "string",
      "canEdit": "string",
      "canView": "string",
      "companies": [
        {}
      ],
      "completed": {},
      "created": {},
      "deals": [
        {}
      ],
      "end": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isDeleted": "string",
      "isSecret": "string",
      "name": "Ava Chen",
      "owner": {},
      "start": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "type": "string",
      "updated": {},
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allDay` | string |  |
| `canEdit` | string |  |
| `canView` | string |  |
| `companies` | array<object> |  |
| `completed` | object |  |
| `created` | object |  |
| `deals` | array<object> |  |
| `end` | date |  |
| `id` | number |  |
| `isDeleted` | string |  |
| `isSecret` | string |  |
| `name` | string |  |
| `owner` | object |  |
| `start` | date |  |
| `status` | string |  |
| `type` | string |  |
| `updated` | object |  |
| `value` | string |  |

## Native endpoint

Through the native Teamgate API, this operation is `GET /events/{{eventId}}` (base URL `https://api.teamgate.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-activity.md) for the provider-specific parameters and requirements.

