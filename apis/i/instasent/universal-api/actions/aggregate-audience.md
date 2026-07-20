# Instasent: Aggregate Audience



```
GET https://connect.mindcloud.co/v1/universal/instasent/latest/actions/aggregate-audience
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instasent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/aggregate-audience?connectionId=$CONNECTION_ID&project=string&aggregations=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string",
  "aggregations": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instasent/latest/actions/aggregate-audience?${params}`, {
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
| `project` | string | yes | Instasent project uid. Use the uid value from List Projects, not the internal project id. |
| `root` | object | no | Audience filter tree to aggregate. |
| `aggregations` | object | yes | Aggregation definition object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entities": {},
      "metadata": {
        "totalHits": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entities` | object | Aggregation result object keyed by the requested aggregation names |
| `metadata.totalHits` | number | Total number of audience contacts that matched the filter |

## Native endpoint

Through the native Instasent API, this operation is `POST /project/:project/audience/aggregations` (base URL `https://api.instasent.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/aggregate-audience.md) for the provider-specific parameters and requirements.

