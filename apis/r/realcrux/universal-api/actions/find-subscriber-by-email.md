# Realcrux: Find Subscriber By Email



```
GET https://connect.mindcloud.co/v1/universal/realcrux/latest/actions/find-subscriber-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Realcrux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/realcrux/latest/actions/find-subscriber-by-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/realcrux/latest/actions/find-subscriber-by-email?${params}`, {
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
| `email` | string | yes | Email address to search for in Sendcrux. |

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
| `subscribers` | array<object> | Subscribers matching the supplied email address; empty when no match exists. |

## Native endpoint

Through the native Realcrux API, this operation is `GET subscribers/email/:email` (base URL `https://sendcrux.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-subscriber-by-email.md) for the provider-specific parameters and requirements.

