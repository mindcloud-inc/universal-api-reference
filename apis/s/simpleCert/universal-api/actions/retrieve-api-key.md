# SimpleCert: Retrieve API Key



```
POST https://connect.mindcloud.co/v1/universal/simpleCert/latest/actions/retrieve-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleCert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpleCert/latest/actions/retrieve-api-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleCert/latest/actions/retrieve-api-key', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "password": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | SimpleCert account login email. |
| `password` | string | yes | SimpleCert account password. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKey` | string | Generated SimpleCert API key. |

## Native endpoint

Through the native SimpleCert API, this operation is `POST /user/api-key` (base URL `https://app.simplecert.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-api-key.md) for the provider-specific parameters and requirements.

