# Metance: Get Topics

Retrieves topics from the current Metance workspace.

```
GET https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-topics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metance `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-topics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-topics?${params}`, {
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
      "contentsCount": 1,
      "description": "string",
      "followed": true,
      "id": 1,
      "important": true,
      "name": "Ava Chen",
      "topicId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentsCount` | number | Related contents count |
| `description` | string | Topic description |
| `followed` | boolean | Whether the current member follows the topic |
| `id` | number | Topic ID |
| `important` | boolean | Important topic flag |
| `name` | string | Topic name |
| `topicId` | number | Topic identifier |

## Native endpoint

Through the native Metance API, this operation is `GET /topics` (base URL `https://api.metance.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-topics.md) for the provider-specific parameters and requirements.

