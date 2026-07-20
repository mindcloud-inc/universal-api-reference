# Anthropic: List Message Batches

Retrieves message batches from the Anthropic account.

```
GET https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/list-message-batches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anthropic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/list-message-batches?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/list-message-batches?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `beforeId` | string | no | Return results before this message batch ID. |
| `afterId` | string | no | Return results after this message batch ID. |
| `limit` | number | no | Number of items to return per page. Example: `20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "firstId": "string",
      "hasMore": true,
      "lastId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `firstId` | string |  |
| `hasMore` | boolean |  |
| `lastId` | string |  |

## Native endpoint

Through the native Anthropic API, this operation is `GET /v1/messages/batches` (base URL `https://api.anthropic.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-message-batches.md) for the provider-specific parameters and requirements.

