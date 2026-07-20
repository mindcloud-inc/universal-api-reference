# Freepik: Search Sound Effects



```
GET https://connect.mindcloud.co/v1/universal/freepik/latest/actions/search-sound-effects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freepik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freepik/latest/actions/search-sound-effects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freepik/latest/actions/search-sound-effects?${params}`, {
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
| `q` | string | no | Sound effect search query. Default: `click`. |
| `limit` | number | no | Maximum number of sound effects to return. Default: `1`. |
| `offset` | number | no | Zero-based sound effect result offset. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "results": [
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
| `count` | number | Total matching sound effects. |
| `results` | array<object> | Matching sound effects. |

## Native endpoint

Through the native Freepik API, this operation is `GET /v1/sound-effects` (base URL `https://api.freepik.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-sound-effects.md) for the provider-specific parameters and requirements.

