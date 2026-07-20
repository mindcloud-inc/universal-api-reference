# Front: Get Teammate

Retrieves detailed teammate information from Front.

```
GET https://connect.mindcloud.co/v1/universal/front/latest/actions/get-teammate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Front `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/front/latest/actions/get-teammate?connectionId=$CONNECTION_ID&teammateId=tea_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teammateId": "tea_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/front/latest/actions/get-teammate?${params}`, {
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
| `teammateId` | string | yes | The teammate ID. Front also accepts a teammate email as a resource alias. Example: `tea_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "isAdmin": true,
      "isAvailable": true,
      "isBlocked": true,
      "lastName": "Chen",
      "links": {
        "related": {
          "conversations": "https://example.com",
          "inboxes": "https://example.com"
        },
        "self": "https://example.com"
      },
      "type": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `isAdmin` | boolean |  |
| `isAvailable` | boolean |  |
| `isBlocked` | boolean |  |
| `lastName` | string |  |
| `links.related.conversations` | string |  |
| `links.related.inboxes` | string |  |
| `links.self` | string |  |
| `type` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Front API, this operation is `GET /teammates/:teammate_id` (base URL `https://api2.frontapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-teammate.md) for the provider-specific parameters and requirements.

