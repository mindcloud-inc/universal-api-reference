# Kazm: Estimate Transform Job Cost

Retrieves a transform job cost estimate from Kazm.

```
GET https://connect.mindcloud.co/v1/universal/kazm/latest/actions/estimate-transform-job-cost
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kazm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kazm/latest/actions/estimate-transform-job-cost?connectionId=$CONNECTION_ID&config=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "config": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kazm/latest/actions/estimate-transform-job-cost?${params}`, {
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
| `config` | object | yes | Transform job configuration payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "steps": [
        {}
      ],
      "total_cost_dollars": 1,
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `steps` | array<object> |  |
| `total_cost_dollars` | number |  |
| `usage` | object |  |

## Native endpoint

Through the native Kazm API, this operation is `POST /transform-jobs/cost-estimation` (base URL `https://api.lightningrod.ai/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/estimate-transform-job-cost.md) for the provider-specific parameters and requirements.

