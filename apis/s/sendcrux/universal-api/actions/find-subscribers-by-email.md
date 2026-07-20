# Sendcrux: Find Subscribers By Email

Finds subscribers in Sendcrux by email address.

```
GET https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/find-subscribers-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendcrux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/find-subscribers-by-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/find-subscribers-by-email?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The email address used to find matching subscribers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "subscribers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `subscribers` | array<object> |  |

## Native endpoint

Through the native Sendcrux API, this operation is `GET /api/v1/subscribers/email/:email` (base URL `https://sendcrux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-subscribers-by-email.md) for the provider-specific parameters and requirements.

