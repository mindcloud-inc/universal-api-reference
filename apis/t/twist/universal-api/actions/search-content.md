# Twist: Search Content

Finds threads and messages in Twist by query.

```
GET https://connect.mindcloud.co/v1/universal/twist/latest/actions/search-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twist/latest/actions/search-content?connectionId=$CONNECTION_ID&query=string&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string",
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twist/latest/actions/search-content?${params}`, {
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
| `cursorMark` | string | no | Token used for pagination. |
| `limit` | number | no | Limits the number of results returned. |
| `query` | string | yes | The full-text query to search for. |
| `title` | string | no | Filter by thread or conversation title. |
| `type` | string | no | Filter by object type: threads, messages, or all. |
| `workspaceId` | number | yes | The workspace to search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversationId": 1,
      "id": "string",
      "messageId": 1,
      "snippet": "string",
      "snippetCreatorId": 1,
      "snippetLastUpdatedTs": 1,
      "title": "string",
      "type": "string",
      "userIds": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversationId` | number |  |
| `id` | string |  |
| `messageId` | number |  |
| `snippet` | string |  |
| `snippetCreatorId` | number |  |
| `snippetLastUpdatedTs` | number |  |
| `title` | string |  |
| `type` | string |  |
| `userIds[]` | number |  |

## Native endpoint

Through the native Twist API, this operation is `GET /search` (base URL `https://api.twist.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-content.md) for the provider-specific parameters and requirements.

