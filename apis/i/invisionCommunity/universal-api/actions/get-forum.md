# Invision Community: Get Forum



```
GET https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-forum
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invision Community `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-forum?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-forum?${params}`, {
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
| `id` | string | yes | The forum identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "topics": 1,
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Forum identifier. |
| `name` | string | Forum name. |
| `topics` | number | Topic count for the forum. |
| `type` | string | Forum type. |
| `url` | string | Absolute URL to the forum. |

## Native endpoint

Through the native Invision Community API, this operation is `GET /forums/forums/:id` (base URL `{{credentials.communityBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-forum.md) for the provider-specific parameters and requirements.

