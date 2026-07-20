# Chat Aid: Get Completion Result

Retrieves a Chat Aid completion result by prompt ID.

```
GET https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/get-completion-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chat Aid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/get-completion-result?connectionId=$CONNECTION_ID&promptId=65e1c08202791119fbe1d476" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "promptId": "65e1c08202791119fbe1d476"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/get-completion-result?${params}`, {
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
| `promptId` | string | yes | Unique question identifier returned by Submit Question. Example: `65e1c08202791119fbe1d476`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canPoll": true,
      "response": "string",
      "sources": {
        "formatted": "string",
        "raw": [
          [
            {}
          ]
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canPoll` | boolean |  |
| `response` | string |  |
| `sources.formatted` | string |  |
| `sources.raw[]` | array<object> |  |
| `sources.raw[].name` | string |  |
| `sources.raw[].provider` | string |  |
| `sources.raw[].url` | string |  |

## Native endpoint

Through the native Chat Aid API, this operation is `GET /chat/completions/custom/:promptId` (base URL `https://api.chataid.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-completion-result.md) for the provider-specific parameters and requirements.

