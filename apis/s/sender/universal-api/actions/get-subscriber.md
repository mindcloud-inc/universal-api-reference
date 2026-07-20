# Sender: Get Subscriber



```
GET https://connect.mindcloud.co/v1/universal/sender/latest/actions/get-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sender/latest/actions/get-subscriber?connectionId=$CONNECTION_ID&subscriberKey=user%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriberKey": "user@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sender/latest/actions/get-subscriber?${params}`, {
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
| `subscriberKey` | string | yes | Subscriber email address, phone number, or ID. Example: `user@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bouncedAt": "2026-05-07T12:00:00.000Z",
      "columns": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstname": "Ava",
      "id": "string",
      "ipAddress": "string",
      "lastname": "Chen",
      "location": "string",
      "phone": "string",
      "phoneCountry": "string",
      "source": "string",
      "status": {},
      "subscriberTags": [
        {}
      ],
      "unsubscribedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bouncedAt` | date |  |
| `columns` | array<object> |  |
| `created` | date |  |
| `email` | string |  |
| `firstname` | string |  |
| `id` | string |  |
| `ipAddress` | string |  |
| `lastname` | string |  |
| `location` | string |  |
| `phone` | string |  |
| `phoneCountry` | string |  |
| `source` | string |  |
| `status` | object |  |
| `subscriberTags` | array<object> |  |
| `unsubscribedAt` | date |  |

## Native endpoint

Through the native Sender API, this operation is `GET /subscribers/:subscriberKey` (base URL `https://api.sender.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber.md) for the provider-specific parameters and requirements.

