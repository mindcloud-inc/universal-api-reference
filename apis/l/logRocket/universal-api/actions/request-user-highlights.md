# LogRocket: Request User Highlights



```
POST https://connect.mindcloud.co/v1/universal/logRocket/latest/actions/request-user-highlights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogRocket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logRocket/latest/actions/request-user-highlights" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logRocket/latest/actions/request-user-highlights', {
  method: 'POST',
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
| `userEmail` | string | no | Email of a user identified in LogRocket. Either User Email or User ID is required by LogRocket. Example: `user@example.com`. |
| `userID` | string | no | ID of a user identified in LogRocket. Either User Email or User ID is required by LogRocket. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `question` | string | no | Optional question for Galileo to answer about the selected sessions. |
| `timeRange` | object | no | Optional object with startMs and endMs epoch millisecond values. Example: `[object Object]`. |
| `webhookURL` | string | no | Optional URL where LogRocket should POST highlights when ready. Example: `https://example.com/webhook`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Highlights request ID used to retrieve results |

## Native endpoint

Through the native LogRocket API, this operation is `POST /orgs/:orgId/apps/:projectId/highlights/` (base URL `https://api.logrocket.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-user-highlights.md) for the provider-specific parameters and requirements.

