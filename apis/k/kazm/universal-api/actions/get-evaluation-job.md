# Kazm: Get Evaluation Job

Retrieves an evaluation job from Kazm.

```
GET https://connect.mindcloud.co/v1/universal/kazm/latest/actions/get-evaluation-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kazm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kazm/latest/actions/get-evaluation-job?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kazm/latest/actions/get-evaluation-job?${params}`, {
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
      "config": {},
      "cost_dollars": 1,
      "created_at": "string",
      "id": "string",
      "status": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object |  |
| `cost_dollars` | number |  |
| `created_at` | string |  |
| `id` | string |  |
| `status` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Kazm API, this operation is `GET /evaluations/:evalId` (base URL `https://api.lightningrod.ai/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-evaluation-job.md) for the provider-specific parameters and requirements.

