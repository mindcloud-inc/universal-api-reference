# Reportei: List Metrics

Retrieves metrics from Reportei.

```
GET https://connect.mindcloud.co/v1/universal/reportei/latest/actions/list-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reportei `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reportei/latest/actions/list-metrics?connectionId=$CONNECTION_ID&limit=25&offset=0&integrationSlug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "integrationSlug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reportei/latest/actions/list-metrics?${params}`, {
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
| `integrationSlug` | string | yes | Slug da integração. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "component": "string",
          "id": "string",
          "reference_key": "string"
        }
      ],
      "meta": {
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].component` | string | Metric component type |
| `data[].id` | string | Metric identifier |
| `data[].reference_key` | string | Metric reference key |
| `meta.total` | number | Total number of metrics |

## Native endpoint

Through the native Reportei API, this operation is `GET /metrics` (base URL `https://app.reportei.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-metrics.md) for the provider-specific parameters and requirements.

