# Cerbo: List Deltas

Retrieves Cerbo delta changes for a resource type.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-deltas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-deltas?connectionId=$CONNECTION_ID&resource_type=string&start_date=string&end_date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resource_type": "string",
  "start_date": "string",
  "end_date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-deltas?${params}`, {
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
| `resource_type` | string | yes | Resource type. Valid resources include `appointments`, `rxs`, `pt_rx`, `drugs`, `supplements`, `orders`, `pt_orders`, `documents`, `patients`, `users`, `tags`, `pt_tags`, `tasks`. |
| `start_date` | string | yes | Starting date of the date range. The start date should be formatted as `YYYY-MM-DD`. The start date can also include time, and should be formatted as `YYYY-MM-DD HH:MM:SS`. |
| `end_date` | string | yes | Ending date of the date range. The end date should be formatted as `YYYY-MM-DD`. The end date can also include time, and should be formatted as `YYYY-MM-DD HH:MM:SS`. The end date must be later than the start date, but can **NOT** be longer than a week in length. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "delta_data": {},
      "from_date": "2026-05-07T12:00:00.000Z",
      "object": "string",
      "resource_type": "string",
      "until_date": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `delta_data` | object |  |
| `from_date` | date |  |
| `object` | string |  |
| `resource_type` | string |  |
| `until_date` | date |  |

## Native endpoint

Through the native Cerbo API, this operation is `GET /delta/:resource_type` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deltas.md) for the provider-specific parameters and requirements.

