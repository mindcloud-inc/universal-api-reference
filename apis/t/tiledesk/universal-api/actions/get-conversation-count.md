# Tiledesk: Get Conversation Count

Retrieves the conversation count from Tiledesk.

```
GET https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/get-conversation-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiledesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/get-conversation-count?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/get-conversation-count?${params}`, {
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
      "_id": "string",
      "count": 1,
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `count` | number |  |
| `value` | number |  |

## Native endpoint

Through the native Tiledesk API, this operation is `GET /{{credentials.projectId}}/analytics/requests/count` (base URL `https://api.tiledesk.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation-count.md) for the provider-specific parameters and requirements.

