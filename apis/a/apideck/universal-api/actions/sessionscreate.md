# Apideck: Create session

Creates a Hosted Vault session in Apideck.

```
POST https://connect.mindcloud.co/v1/universal/apideck/latest/actions/sessionscreate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apideck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/apideck/latest/actions/sessionscreate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apideck/latest/actions/sessionscreate', {
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
| `consumer_metadata` | object | no |  |
| `redirect_uri` | string | no |  |
| `settings` | object | no |  |
| `theme` | object | no |  |
| `custom_consumer_settings` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "session_token": "string",
      "session_uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `session_token` | string |  |
| `session_uri` | string |  |

## Native endpoint

Through the native Apideck API, this operation is `POST /vault/sessions` (base URL `https://unify.apideck.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sessionscreate.md) for the provider-specific parameters and requirements.

