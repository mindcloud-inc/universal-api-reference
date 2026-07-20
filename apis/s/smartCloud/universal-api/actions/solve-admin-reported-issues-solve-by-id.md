# 2Smart Cloud: Set report as solved



```
PUT https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/solve-admin-reported-issues-solve-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/solve-admin-reported-issues-solve-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/solve-admin-reported-issues-solve-by-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of entity |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "message": "string",
      "product_id": 1,
      "solved": true,
      "status": "string",
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "user_id": 1,
      "vendor_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `id` | number |  |
| `message` | string |  |
| `product_id` | number |  |
| `solved` | boolean |  |
| `status` | string |  |
| `type` | string |  |
| `updated` | date |  |
| `user_id` | number |  |
| `vendor_id` | number |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `POST /admin/reported-issues/solve/{id}` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/solve-admin-reported-issues-solve-by-id.md) for the provider-specific parameters and requirements.

