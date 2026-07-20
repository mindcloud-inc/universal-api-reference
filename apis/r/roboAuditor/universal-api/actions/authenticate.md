# RoboAuditor: Authenticate



```
POST https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/authenticate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RoboAuditor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/authenticate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "{{credentials.email}}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/authenticate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "{{credentials.email}}"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Login email. Default: `{{credentials.email}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_token": "string",
      "expires_in": 1,
      "refresh_token": "string",
      "token_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_token` | string |  |
| `expires_in` | number |  |
| `refresh_token` | string |  |
| `token_type` | string |  |

## Native endpoint

Through the native RoboAuditor API, this operation is `POST /login` (base URL `https://app.siteauditor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authenticate.md) for the provider-specific parameters and requirements.

