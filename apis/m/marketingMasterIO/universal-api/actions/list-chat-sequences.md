# Marketing Master IO: List Chat Sequences

Retrieves chat sequences from Marketing Master IO.

```
GET https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/list-chat-sequences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Marketing Master IO `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/list-chat-sequences?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/list-chat-sequences?${params}`, {
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
| `page_id` | string | no | Filter chat sequences by Facebook page ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date_created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "page_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date_created` | date |  |
| `id` | string |  |
| `name` | string |  |
| `page_id` | string |  |

## Native endpoint

Through the native Marketing Master IO API, this operation is `GET /v1/messenger/chat_sequences` (base URL `https://api.marketingmaster.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-chat-sequences.md) for the provider-specific parameters and requirements.

