# Ritekit: Get Hashtag Suggestions For Text

Retrieves Ritekit hashtag suggestions for text.

```
GET https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-hashtag-suggestions-for-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ritekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-hashtag-suggestions-for-text?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-hashtag-suggestions-for-text?${params}`, {
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
| `text` | string | yes | Text to analyze for hashtag suggestions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": [
        {}
      ],
      "message": "string",
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | array<object> |  |
| `message` | string |  |
| `result` | boolean |  |

## Native endpoint

Through the native Ritekit API, this operation is `GET /v1/stats/hashtag-suggestions` (base URL `https://api.ritekit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hashtag-suggestions-for-text.md) for the provider-specific parameters and requirements.

