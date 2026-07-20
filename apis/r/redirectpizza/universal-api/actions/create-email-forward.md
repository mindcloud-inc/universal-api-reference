# redirect.pizza: Create Email Forward



```
POST https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/create-email-forward
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a redirect.pizza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/create-email-forward" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "alias": "string",
  "domain": "string",
  "destination": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/create-email-forward', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "alias": "string",
    "domain": "string",
    "destination": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `alias` | string | yes | Alias before the @ sign. Use * for a catch-all forward. |
| `domain` | string | yes | Domain that receives the forwarded email. |
| `destination` | string | yes | Destination email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "createdAt": "string",
      "destination": "string",
      "domain": "string",
      "id": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `createdAt` | string |  |
| `destination` | string |  |
| `domain` | string |  |
| `id` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native redirect.pizza API, this operation is `POST /api/v1/email-forwards` (base URL `https://redirect.pizza`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-email-forward.md) for the provider-specific parameters and requirements.

