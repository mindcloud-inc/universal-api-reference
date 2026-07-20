# Invidious: Get Hashtag Results



```
GET https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-hashtag-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-hashtag-results?connectionId=$CONNECTION_ID&tag=music" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tag": "music"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-hashtag-results?${params}`, {
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
| `page` | number | no | Hashtag result page number. Example: `1`. |
| `tag` | string | yes | Hashtag without the # prefix. Example: `music`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "continuation": "string",
      "tag": "string",
      "videos": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `continuation` | string |  |
| `tag` | string |  |
| `videos` | array<object> |  |

## Native endpoint

Through the native Invidious API, this operation is `GET /hashtag/:tag` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hashtag-results.md) for the provider-specific parameters and requirements.

