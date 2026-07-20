# Podscan: Get Podcast Brand Safety

Retrieves podcast brand safety details from Podscan.

```
GET https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-podcast-brand-safety
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-podcast-brand-safety?connectionId=$CONNECTION_ID&podcast=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "podcast": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-podcast-brand-safety?${params}`, {
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
| `podcast` | string | yes | The podcast ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aggregation": {},
      "categories": [
        {}
      ],
      "framework": "string",
      "note": "string",
      "podcast_id": "string",
      "podcast_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aggregation` | object |  |
| `categories` | array<object> |  |
| `framework` | string |  |
| `note` | string |  |
| `podcast_id` | string |  |
| `podcast_name` | string |  |

## Native endpoint

Through the native Podscan API, this operation is `GET /podcasts/{podcast}/brand-safety` (base URL `https://podscan.fm/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-podcast-brand-safety.md) for the provider-specific parameters and requirements.

