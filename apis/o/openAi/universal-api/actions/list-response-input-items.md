# Open AI: List Response Input Items

Retrieves input items from a response in Open AI.

```
GET https://connect.mindcloud.co/v1/universal/openAi/latest/actions/list-response-input-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/list-response-input-items?connectionId=$CONNECTION_ID&response_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "response_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openAi/latest/actions/list-response-input-items?${params}`, {
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
| `response_id` | string | yes | The ID of the response whose input items are listed. |
| `limit` | date | no | Maximum number of input items to return. |
| `order` | list | no | Sort order for returned items. Default: `asc`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `after` | string | no | Return items after this cursor. |
| `before` | string | no | Return items before this cursor. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "content": [
            {
              "text": "string",
              "type": "string"
            }
          ],
          "id": "string",
          "role": "string",
          "status": "string",
          "type": "string"
        }
      ],
      "firstId": "string",
      "hasMore": true,
      "lastId": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].content[].text` | string |  |
| `data[].content[].type` | string |  |
| `data[].id` | string |  |
| `data[].role` | string |  |
| `data[].status` | string |  |
| `data[].type` | string |  |
| `firstId` | string |  |
| `hasMore` | boolean |  |
| `lastId` | string |  |
| `object` | string |  |

## Native endpoint

Through the native Open AI API, this operation is `GET v1/responses/:response_id/input_items` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-response-input-items.md) for the provider-specific parameters and requirements.

