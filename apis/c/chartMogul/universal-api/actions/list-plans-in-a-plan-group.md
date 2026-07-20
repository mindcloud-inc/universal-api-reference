# ChartMogul: List Plans in a Plan Group

Retrieves plans in a plan group from ChartMogul.

```
GET https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-plans-in-a-plan-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChartMogul `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-plans-in-a-plan-group?connectionId=$CONNECTION_ID&limit=25&offset=0&planGroupUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "planGroupUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-plans-in-a-plan-group?${params}`, {
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
| `planGroupUuid` | string | yes | The ChartMogul UUID of the plan group whose plans you want to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataSourceUuid": "string",
      "externalId": "string",
      "intervalCount": 1,
      "intervalUnit": "string",
      "name": "Ava Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataSourceUuid` | string |  |
| `externalId` | string |  |
| `intervalCount` | number |  |
| `intervalUnit` | string |  |
| `name` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native ChartMogul API, this operation is `GET /plan_groups/:planGroupUuid/plans` (base URL `https://api.chartmogul.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-plans-in-a-plan-group.md) for the provider-specific parameters and requirements.

