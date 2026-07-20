# BuildBetter: List Conversations



```
GET https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildBetter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-conversations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-conversations?${params}`, {
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
| `limit` | number | no | Maximum number of conversations to return. Default: `25`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "display_ts": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "interaction": "string",
      "is_open": true,
      "platform": "string",
      "platform_updated_at": "2026-05-07T12:00:00.000Z",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `display_ts` | date | Display timestamp. |
| `id` | string | BuildBetter conversation identifier. |
| `interaction` | string | Interaction summary. |
| `is_open` | boolean | Whether the conversation is still open. |
| `platform` | string | Conversation platform. |
| `platform_updated_at` | date | Platform updated timestamp. |
| `title` | string | Conversation title. |

## Native endpoint

Through the native BuildBetter API, this operation is `POST /graphql` (base URL `https://api.buildbetter.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

