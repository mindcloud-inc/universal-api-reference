# Ritekit: Clean Banned Instagram Hashtags

Removes banned Instagram hashtags with Ritekit.

```
GET https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/clean-banned-instagram-hashtags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ritekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/clean-banned-instagram-hashtags?connectionId=$CONNECTION_ID&post=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "post": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/clean-banned-instagram-hashtags?${params}`, {
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
| `post` | string | yes | Hashtag string to clean for banned Instagram hashtags. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bannedHashtags": [
        "string"
      ],
      "message": "string",
      "post": "string",
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bannedHashtags` | array<string> |  |
| `message` | string |  |
| `post` | string |  |
| `result` | boolean |  |

## Native endpoint

Through the native Ritekit API, this operation is `GET /v2/instagram/hashtags-cleaner` (base URL `https://api.ritekit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clean-banned-instagram-hashtags.md) for the provider-specific parameters and requirements.

