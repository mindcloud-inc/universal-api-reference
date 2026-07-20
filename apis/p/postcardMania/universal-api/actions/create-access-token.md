# PostcardMania: Create Access Token

Creates a new access token in PostcardMania.

```
POST https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/create-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostcardMania `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/create-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "apiKey": "string",
  "apiSecret": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/create-access-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "apiKey": "string",
    "apiSecret": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `apiKey` | string | yes | Raw PCM portal API key. |
| `apiSecret` | string | yes | Raw PCM portal API secret. |
| `childRefNbr` | string | no | Optional child app account reference. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expires": "2026-05-07T12:00:00.000Z",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expires` | date | Expiration timestamp for the bearer token. |
| `token` | string | Bearer token for subsequent API calls. |

## Native endpoint

Through the native PostcardMania API, this operation is `POST /auth/login` (base URL `https://v3.pcmintegrations.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-access-token.md) for the provider-specific parameters and requirements.

