# BlazeMeter: Regenerate User API Key Secret



```
PUT https://connect.mindcloud.co/v1/universal/blazeMeter/latest/actions/regenerate-user-api-key-secret
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlazeMeter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blazeMeter/latest/actions/regenerate-user-api-key-secret" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "apiKeyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blazeMeter/latest/actions/regenerate-user-api-key-secret', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "apiKeyId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `apiKeyId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "id": "string",
      "message": "string",
      "meta": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Provider response payload. |
| `id` | string | Optional response identifier. |
| `message` | string | Optional response message. |
| `meta` | object | Execution metadata including request/response details. |
| `success` | boolean | Whether the action run succeeded. |

## Native endpoint

Through the native BlazeMeter API, this operation is `POST /user/api-keys/:apiKeyId/regenerate` (base URL `https:///a.blazemeter.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/regenerate-user-api-key-secret.md) for the provider-specific parameters and requirements.

