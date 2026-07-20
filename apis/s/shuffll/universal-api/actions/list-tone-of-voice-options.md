# Shuffll: List Tone of Voice Options

Retrieves tone of voice options from Shuffll.

```
GET https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/list-tone-of-voice-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/list-tone-of-voice-options?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/list-tone-of-voice-options?${params}`, {
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
      "tones": [
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
| `tones` | array<object> | Available tone of voice options. |

## Native endpoint

Through the native Shuffll API, this operation is `GET /auth/config/tone_of_voice` (base URL `https://api.shuffll.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tone-of-voice-options.md) for the provider-specific parameters and requirements.

