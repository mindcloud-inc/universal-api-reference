# SignRequest: List Webhooks



```
GET https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignRequest `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/list-webhooks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "callbackUrl": "https://example.com",
      "created": "2026-05-07T12:00:00.000Z",
      "eventType": "string",
      "integration": "string",
      "name": "Ava Chen",
      "url": "https://example.com",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callbackUrl` | string |  |
| `created` | date |  |
| `eventType` | string |  |
| `integration` | string |  |
| `name` | string |  |
| `url` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native SignRequest API, this operation is `GET /webhooks/` (base URL `https://signrequest.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

