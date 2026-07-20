# Coresignal: Bulk Collect Multi-source Employees By IDs

Creates a bulk multi-source employee collection request in Coresignal.

```
POST https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/bulk-collect-multi-source-employees-by-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coresignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/bulk-collect-multi-source-employees-by-ids" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ids[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/bulk-collect-multi-source-employees-by-ids', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ids[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ids[]` | array<number> | yes |  |

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

Through the native Coresignal API, this operation is `POST /data_requests/employee_multi_source/ids` (base URL `https://api.coresignal.com/cdapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-collect-multi-source-employees-by-ids.md) for the provider-specific parameters and requirements.

