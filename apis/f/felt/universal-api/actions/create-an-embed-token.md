# Felt: Create An Embed Token

Creates a short-lived embed token in Felt.

```
POST https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-an-embed-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-an-embed-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mapId": "string",
  "userEmail": "apps@mindcloud.co"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/felt/latest/actions/create-an-embed-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mapId": "string",
    "userEmail": "apps@mindcloud.co"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mapId` | string | yes | The ID of the map. |
| `userEmail` | string | yes | The workspace member email that will use the embed token. Example: `apps@mindcloud.co`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expires_at": "2026-05-07T12:00:00.000Z",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expires_at` | date | Token expiration timestamp. |
| `token` | string | Short-lived embed token. |

## Native endpoint

Through the native Felt API, this operation is `POST /maps/:mapId/embed_token` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-an-embed-token.md) for the provider-specific parameters and requirements.

