# Dify: Get Next Suggested Questions

Retrieves suggested questions from Dify.

```
GET https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-next-suggested-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-next-suggested-questions?connectionId=$CONNECTION_ID&messageId=string&user=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string",
  "user": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-next-suggested-questions?${params}`, {
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
| `messageId` | string | yes | Message ID to fetch suggestions for. |
| `user` | string | yes | User identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string |  |

## Native endpoint

Through the native Dify API, this operation is `GET /messages/:message_id/suggested` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-next-suggested-questions.md) for the provider-specific parameters and requirements.

