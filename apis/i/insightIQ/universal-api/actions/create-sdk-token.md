# InsightIQ: Create SDK Token

Creates a new SDK token in InsightIQ.

```
POST https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/create-sdk-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InsightIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/create-sdk-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "products[]": [
    "string"
  ],
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/create-sdk-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "products[]": ["string"],
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `products[]` | array<string> | yes | Products to enable in the SDK token. |
| `userId` | string | yes | InsightIQ user identifier used to mint the SDK token. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expires_at": "2026-05-07T12:00:00.000Z",
      "sdk_token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expires_at` | date |  |
| `sdk_token` | string |  |

## Native endpoint

Through the native InsightIQ API, this operation is `POST /v1/sdk-tokens` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sdk-token.md) for the provider-specific parameters and requirements.

