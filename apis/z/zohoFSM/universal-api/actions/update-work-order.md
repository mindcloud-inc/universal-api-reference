# Zoho FSM: Update Work Order

Updates an existing work order in Zoho FSM.

```
PUT https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/update-work-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho FSM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/update-work-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recordId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/update-work-order', {
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
| `data[0].Service_Line_Items[0].$fsm_delete` | boolean | no |  |
| `data[0].Service_Line_Items[0].id` | string | no |  |
| `data[0].Service_Line_Items[0].Part_Line_Items[0].$fsm_delete` | boolean | no |  |
| `data[0].Service_Line_Items[0].Part_Line_Items[0].id` | string | no |  |
| `data[0].Service_Line_Items[0].Quantity` | number | no |  |
| `data[0].Summary` | string | no |  |
| `recordId` | string | yes | The Zoho FSM record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "details": {
        "createdBy": {
          "id": "string",
          "name": "Ava Chen"
        },
        "createdTime": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "modifiedBy": {
          "id": "string",
          "name": "Ava Chen"
        },
        "modifiedTime": "2026-05-07T12:00:00.000Z"
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
| `code` | string |  |
| `details.createdBy.id` | string |  |
| `details.createdBy.name` | string |  |
| `details.createdTime` | date |  |
| `details.id` | string |  |
| `details.modifiedBy.id` | string |  |
| `details.modifiedBy.name` | string |  |
| `details.modifiedTime` | date |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho FSM API, this operation is `PUT /Work_Orders/:recordId` (base URL `{{credentials.accessTokenRequest.api_domain}}/fsm/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-work-order.md) for the provider-specific parameters and requirements.

