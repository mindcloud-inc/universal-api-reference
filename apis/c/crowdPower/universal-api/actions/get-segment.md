# CrowdPower: Get Segment

Retrieves a segment from CrowdPower.

```
GET https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CrowdPower `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-segment?connectionId=$CONNECTION_ID&segmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "segmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-segment?${params}`, {
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
| `segmentId` | string | yes | Segment identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": 1,
      "customers_count": 1,
      "deleted_at": 1,
      "id": "string",
      "name": "Ava Chen",
      "op": "string",
      "rules": [
        {}
      ],
      "slug": "string",
      "synced_at": 1,
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | number |  |
| `customers_count` | number |  |
| `deleted_at` | number |  |
| `id` | string |  |
| `name` | string |  |
| `op` | string |  |
| `rules` | array<object> |  |
| `slug` | string |  |
| `synced_at` | number |  |
| `updated_at` | number |  |

## Native endpoint

Through the native CrowdPower API, this operation is `GET segments/:segment_id` (base URL `https://api.crowdpower.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-segment.md) for the provider-specific parameters and requirements.

