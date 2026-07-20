# Rollbar: Update Access Token Rate Limit By Path

Updates a project access token rate limit in Rollbar by path identifier.

```
PUT https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/update-access-token-rate-limit-by-path
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rollbar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/update-access-token-rate-limit-by-path" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "tokenIdentifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/update-access-token-rate-limit-by-path', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "tokenIdentifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | Rollbar project identifier |
| `tokenIdentifier` | string | yes | Project access token identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "err": 1,
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `err` | number |  |
| `result` | object |  |

## Native endpoint

Through the native Rollbar API, this operation is `PATCH /project/:projectId/access_token/:tokenIdentifier` (base URL `https://api.rollbar.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-access-token-rate-limit-by-path.md) for the provider-specific parameters and requirements.

