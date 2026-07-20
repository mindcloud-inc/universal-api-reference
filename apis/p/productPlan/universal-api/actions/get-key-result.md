# ProductPlan: Get Key Result

Retrieves a key result from ProductPlan.

```
GET https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-key-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProductPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-key-result?connectionId=$CONNECTION_ID&id=string&objectiveId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "objectiveId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-key-result?${params}`, {
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
| `id` | string | yes |  |
| `objectiveId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "current": 1,
      "description": "string",
      "id": 1,
      "progress": 1,
      "start": 1,
      "target": 1,
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `current` | number |  |
| `description` | string |  |
| `id` | number |  |
| `progress` | number |  |
| `start` | number |  |
| `target` | number |  |
| `type` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native ProductPlan API, this operation is `GET /strategy/objectives/:objective_id/key_results/:id` (base URL `https://app.productplan.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-key-result.md) for the provider-specific parameters and requirements.

