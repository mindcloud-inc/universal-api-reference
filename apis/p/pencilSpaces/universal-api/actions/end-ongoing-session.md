# Pencil Spaces: End Ongoing Session



```
PUT https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/end-ongoing-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pencil Spaces `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/end-ongoing-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/end-ongoing-session', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spaceId` | string | yes | The Space with an ongoing session to end. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endedSessionId": "string",
      "newSessionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endedSessionId` | string |  |
| `newSessionId` | string |  |

## Native endpoint

Through the native Pencil Spaces API, this operation is `POST /spaces/:spaceId/endOngoingSession` (base URL `https://apis.pencilapp.com/public/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/end-ongoing-session.md) for the provider-specific parameters and requirements.

