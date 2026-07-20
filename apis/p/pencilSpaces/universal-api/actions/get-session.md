# Pencil Spaces: Get Session



```
GET https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/get-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pencil Spaces `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/get-session?connectionId=$CONNECTION_ID&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/get-session?${params}`, {
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
| `sessionId` | string | yes | The session to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendees": [
        {}
      ],
      "recordings": [
        {}
      ],
      "sessionEndTime": "string",
      "sessionId": "string",
      "sessionStartTime": "string",
      "sessionStats": {},
      "sessionTitle": "string",
      "sessionVisibility": "string",
      "spaceId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendees` | array<object> |  |
| `recordings` | array<object> |  |
| `sessionEndTime` | string |  |
| `sessionId` | string |  |
| `sessionStartTime` | string |  |
| `sessionStats` | object |  |
| `sessionTitle` | string |  |
| `sessionVisibility` | string |  |
| `spaceId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Pencil Spaces API, this operation is `GET /analytics/sessions/:sessionId` (base URL `https://apis.pencilapp.com/public/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session.md) for the provider-specific parameters and requirements.

