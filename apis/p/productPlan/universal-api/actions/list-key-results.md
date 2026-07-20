# ProductPlan: List Key Results

Lists key results for an objective in ProductPlan.

```
GET https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/list-key-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProductPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/list-key-results?connectionId=$CONNECTION_ID&objectiveId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "objectiveId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/list-key-results?${params}`, {
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
| `objectiveId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "paging": {},
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `paging` | object | Pagination metadata for the response. |
| `results` | array<object> | Collection of records returned by this ProductPlan list endpoint. |

## Native endpoint

Through the native ProductPlan API, this operation is `GET /strategy/objectives/:objective_id/key_results` (base URL `https://app.productplan.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-key-results.md) for the provider-specific parameters and requirements.

