# Kazm: Estimate Training Cost

Retrieves a training cost estimate from Kazm.

```
GET https://connect.mindcloud.co/v1/universal/kazm/latest/actions/estimate-training-cost
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kazm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kazm/latest/actions/estimate-training-cost?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kazm/latest/actions/estimate-training-cost?${params}`, {
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
      "effective_steps": 1,
      "prefill_tokens": 1,
      "sample_tokens": 1,
      "total_cost_dollars": 1,
      "train_tokens": 1,
      "warning_message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `effective_steps` | number |  |
| `prefill_tokens` | number |  |
| `sample_tokens` | number |  |
| `total_cost_dollars` | number |  |
| `train_tokens` | number |  |
| `warning_message` | string |  |

## Native endpoint

Through the native Kazm API, this operation is `POST /training-jobs/cost-estimation` (base URL `https://api.lightningrod.ai/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/estimate-training-cost.md) for the provider-specific parameters and requirements.

