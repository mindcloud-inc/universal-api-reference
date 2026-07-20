# Hume: Get job predictions



```
GET https://connect.mindcloud.co/v1/universal/hume/latest/actions/get-job-predictions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hume `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hume/latest/actions/get-job-predictions?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hume/latest/actions/get-job-predictions?${params}`, {
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
| `id` | string | yes | Expression Measurement job identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "predictions": [
        {}
      ],
      "results": [
        {}
      ],
      "source": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `predictions` | array<object> |  |
| `results` | array<object> |  |
| `source` | object |  |

## Native endpoint

Through the native Hume API, this operation is `GET /v0/batch/jobs/:id/predictions` (base URL `https://api.hume.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-predictions.md) for the provider-specific parameters and requirements.

