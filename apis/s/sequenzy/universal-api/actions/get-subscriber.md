# Sequenzy: Get Subscriber

Retrieves a subscriber from Sequenzy by email address.

```
GET https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/get-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sequenzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/get-subscriber?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/get-subscriber?${params}`, {
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
| `email` | string | yes | Subscriber email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "subscriber": {
        "createdAt": "string",
        "customAttributes": {},
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "status": "string",
        "tags": [
          "string"
        ],
        "updatedAt": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `subscriber.createdAt` | string |  |
| `subscriber.customAttributes` | object |  |
| `subscriber.email` | string |  |
| `subscriber.firstName` | string |  |
| `subscriber.id` | string |  |
| `subscriber.lastName` | string |  |
| `subscriber.status` | string |  |
| `subscriber.tags` | array<string> |  |
| `subscriber.updatedAt` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Sequenzy API, this operation is `GET /subscribers/:email` (base URL `https://api.sequenzy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber.md) for the provider-specific parameters and requirements.

