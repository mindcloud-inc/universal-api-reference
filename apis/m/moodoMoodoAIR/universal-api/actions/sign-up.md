# Moodo & Moodo AIR: Sign Up

Creates a Moodo user and returns a token.

```
POST https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/sign-up
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moodo & Moodo AIR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/sign-up" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/sign-up', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `token` | string |  |

## Native endpoint

Through the native Moodo & Moodo AIR API, this operation is `POST /signup` (base URL `https://rest.moodo.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sign-up.md) for the provider-specific parameters and requirements.

