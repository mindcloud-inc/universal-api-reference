# Coresignal: Bulk Collect Base Employees By Filters

Creates a bulk base employee collection request in Coresignal.

```
POST https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/bulk-collect-base-employees-by-filters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coresignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/bulk-collect-base-employees-by-filters" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filters": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/bulk-collect-base-employees-by-filters', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filters": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filters` | object | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "request_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `request_id` | string |  |

## Native endpoint

Through the native Coresignal API, this operation is `POST /data_requests/employee_base/filter` (base URL `https://api.coresignal.com/cdapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-collect-base-employees-by-filters.md) for the provider-specific parameters and requirements.

