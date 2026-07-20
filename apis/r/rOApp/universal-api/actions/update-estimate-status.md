# RO App: Update Estimate Status



```
PUT https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/update-estimate-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/update-estimate-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "estimateId": 1,
  "statusId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/update-estimate-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "estimateId": 1,
    "statusId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `estimateId` | number | yes | Estimate ID |
| `statusId` | number | yes | Status Id |
| `comment` | string | no | Status comment |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "comment": "string",
      "group": {
        "name": "Ava Chen",
        "type": 1
      },
      "id": 1,
      "name": "Ava Chen",
      "status_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `comment` | string |  |
| `group` | object |  |
| `group.name` | string |  |
| `group.type` | number |  |
| `id` | number |  |
| `name` | string |  |
| `status_id` | number |  |

## Native endpoint

Through the native RO App API, this operation is `POST /estimates/:estimate_id/status` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-estimate-status.md) for the provider-specific parameters and requirements.

