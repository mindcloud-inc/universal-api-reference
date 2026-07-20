# Livestorm: Get Session

Retrieves a session from Livestorm.

```
GET https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/get-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Livestorm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/get-session?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/get-session?${params}`, {
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
| `id` | string | yes | Session ID |
| `include` | string | no | Include Related Data Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "attendeesCount": 1,
        "canceledAt": 1,
        "createdAt": 1,
        "duration": 1,
        "endedAt": 1,
        "estimatedStartedAt": 1,
        "eventTypeId": "string",
        "name": "Ava Chen",
        "registrantsCount": 1,
        "roomLink": "https://example.com",
        "startedAt": 1,
        "status": "string",
        "timezone": "string",
        "updatedAt": 1
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.attendeesCount` | number |  |
| `attributes.canceledAt` | number |  |
| `attributes.createdAt` | number |  |
| `attributes.duration` | number |  |
| `attributes.endedAt` | number |  |
| `attributes.estimatedStartedAt` | number |  |
| `attributes.eventTypeId` | string |  |
| `attributes.name` | string |  |
| `attributes.registrantsCount` | number |  |
| `attributes.roomLink` | string |  |
| `attributes.startedAt` | number |  |
| `attributes.status` | string |  |
| `attributes.timezone` | string |  |
| `attributes.updatedAt` | number |  |
| `id` | string | ID |
| `type` | string | Type |

## Native endpoint

Through the native Livestorm API, this operation is `GET sessions/:id` (base URL `https://api.livestorm.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session.md) for the provider-specific parameters and requirements.

