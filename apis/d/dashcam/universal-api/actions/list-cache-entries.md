# Dashcam: List Cache Entries

Retrieves cache entries from Dashcam.

```
GET https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/list-cache-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dashcam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/list-cache-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/list-cache-entries?${params}`, {
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
| `limit` | string | no |  |
| `page` | string | no |  |
| `type` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `meta` | object |  |

## Native endpoint

Through the native Dashcam API, this operation is `GET /api/v1/cache/entries` (base URL `https://api.testdriver.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cache-entries.md) for the provider-specific parameters and requirements.

