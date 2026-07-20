# Hoversignal: List Quiz Hooks



```
GET https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/list-quiz-hooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hoversignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/list-quiz-hooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/list-quiz-hooks?${params}`, {
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
      "hooks": [
        {
          "createdAt": "string",
          "errorCount": 1,
          "id": "string",
          "topic": "string",
          "url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hooks` | array<object> | The list of hooks for this Hoversignal hook surface. |
| `hooks[].createdAt` | string | When the hook was created. |
| `hooks[].errorCount` | number | The number of recent delivery errors for the hook. |
| `hooks[].id` | string | The hook identifier. |
| `hooks[].topic` | string | The hook topic. |
| `hooks[].url` | string | The destination URL for the hook. |

## Native endpoint

Through the native Hoversignal API, this operation is `GET /api/v1/hooks/quiz` (base URL `https://app.hoversignal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-quiz-hooks.md) for the provider-specific parameters and requirements.

