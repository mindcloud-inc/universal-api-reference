# Zoho People: Cancel Leave Request

Cancels a leave request in Zoho People.

```
PUT https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/cancel-leave-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/cancel-leave-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recordId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/cancel-leave-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recordId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recordId` | string | yes | Leave request record ID to cancel. |
| `reason` | string | no | Optional reason for cancelling the leave request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": 1
      },
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.id` | number |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho People API, this operation is `PATCH /api/v3/leave-tracker/leaves/:recordId` (base URL `https://people.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-leave-request.md) for the provider-specific parameters and requirements.

