# Fliz: List voices

Retrieves available text-to-speech voices from Fliz.

```
GET https://connect.mindcloud.co/v1/universal/fliz/latest/actions/list-voices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fliz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fliz/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fliz/latest/actions/list-voices?${params}`, {
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
      "gender": "string",
      "id": "string",
      "name": "Ava Chen",
      "samples": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gender` | string | Voice gender. |
| `id` | string | Voice ID. |
| `name` | string | Voice display name. |
| `samples` | object | Language-keyed sample audio URLs. |

## Native endpoint

Through the native Fliz API, this operation is `GET /api/rest/voices` (base URL `https://app.fliz.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-voices.md) for the provider-specific parameters and requirements.

