# Microsoft 365 Planner: List Plan Buckets



```
GET https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/list-plan-buckets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/list-plan-buckets?connectionId=$CONNECTION_ID&planId=xqQg5FS2LkCp935s-FIFm2QAFkHM" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "planId": "xqQg5FS2LkCp935s-FIFm2QAFkHM"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/list-plan-buckets?${params}`, {
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
| `planId` | string | yes | Planner plan ID whose buckets should be listed. Example: `xqQg5FS2LkCp935s-FIFm2QAFkHM`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "orderHint": "string",
      "planId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `orderHint` | string |  |
| `planId` | string |  |

## Native endpoint

Through the native Microsoft 365 Planner API, this operation is `GET /v1.0/planner/plans/{{planId}}/buckets` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-plan-buckets.md) for the provider-specific parameters and requirements.

