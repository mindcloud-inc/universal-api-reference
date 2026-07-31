# Final Space: Get Episode



```
GET https://connect.mindcloud.co/v1/universal/finalSpace/latest/actions/get-episode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Final Space `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finalSpace/latest/actions/get-episode?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finalSpace/latest/actions/get-episode?${params}`, {
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
| `id` | number | yes | Numeric Episode ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "air_date": "string",
      "characters": [
        "string"
      ],
      "director": "string",
      "id": 1,
      "img_url": "https://example.com",
      "name": "Ava Chen",
      "writer": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `air_date` | string |  |
| `characters` | array<string> |  |
| `director` | string |  |
| `id` | number |  |
| `img_url` | string |  |
| `name` | string |  |
| `writer` | string |  |

## Native endpoint

Through the native Final Space API, this operation is `GET /episode/:id` (base URL `https://finalspaceapi.com/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-episode.md) for the provider-specific parameters and requirements.

