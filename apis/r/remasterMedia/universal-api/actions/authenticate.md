# RemasterMedia: Authenticate

Creates an auth token in RemasterMedia.

```
POST https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/authenticate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RemasterMedia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/authenticate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/authenticate', {
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
      "expiration": "2026-05-07T12:00:00.000Z",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiration` | date | Token expiration timestamp. |
| `token` | string | JWT token returned by RemasterMedia authentication. |

## Native endpoint

Through the native RemasterMedia API, this operation is `POST /auth` (base URL `https://api-sandbox.remastermedia.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authenticate.md) for the provider-specific parameters and requirements.

