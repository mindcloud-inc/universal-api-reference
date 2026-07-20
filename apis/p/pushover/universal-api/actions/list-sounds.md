# Pushover: List Sounds



```
GET https://connect.mindcloud.co/v1/universal/pushover/latest/actions/list-sounds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushover `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushover/latest/actions/list-sounds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushover/latest/actions/list-sounds?${params}`, {
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
      "request": "string",
      "sounds": {},
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `request` | string | Pushover request identifier. |
| `sounds` | object | Hash of sound parameter names to human-readable sound labels. |
| `status` | number | API status. Returns 1 when the sound list request succeeds. |

## Native endpoint

Through the native Pushover API, this operation is `GET /sounds.json` (base URL `https://api.pushover.net/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sounds.md) for the provider-specific parameters and requirements.

