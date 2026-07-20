# Ellipsend: Update Status

Updates an existing status in Ellipsend.

```
PUT https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/update-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ellipsend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/update-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "statusId": 1,
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/update-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "statusId": 1,
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `statusId` | number | yes | The status ID. |
| `status` | string | yes | The new status value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Ellipsend API, this operation is `PUT /status/[:status_id]` (base URL `https://api.ellipsend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-status.md) for the provider-specific parameters and requirements.

