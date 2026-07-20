# Hedy: Delete Topic

Deletes a topic from Hedy.

```
DELETE https://connect.mindcloud.co/v1/universal/hedy/latest/actions/delete-topic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hedy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/hedy/latest/actions/delete-topic?connectionId=$CONNECTION_ID&topicId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "topicId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hedy/latest/actions/delete-topic?${params}`, {
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
| `topicId` | string | yes | Unique identifier of the topic. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Hedy API, this operation is `DELETE https://api.hedy.bot/topics/:topicId` (base URL `https://api.hedy.bot`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-topic.md) for the provider-specific parameters and requirements.

