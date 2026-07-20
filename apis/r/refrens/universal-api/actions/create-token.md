# Refrens: Create Token



```
POST https://connect.mindcloud.co/v1/universal/refrens/latest/actions/create-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refrens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/refrens/latest/actions/create-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "appSecret": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/refrens/latest/actions/create-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "appSecret": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Refrens App ID from the API credentials screen. |
| `appSecret` | string | yes | Refrens API Secret paired with the App ID. Use this only to generate an access token. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessToken": "string",
      "appId": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string |  |
| `appId` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Refrens API, this operation is `POST /authentication` (base URL `https://api.refrens.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-token.md) for the provider-specific parameters and requirements.

