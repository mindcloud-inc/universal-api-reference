# Zoho FSM: Perform Work Order Transition

Performs a work order blueprint transition in Zoho FSM.

```
PUT https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/perform-work-order-transition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho FSM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/perform-work-order-transition" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recordId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/perform-work-order-transition', {
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
| `blueprint[].transition_id` | string | no |  |
| `recordId` | string | yes | The Zoho FSM record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "details": {
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
| `details.modifiedTime` | date |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho FSM API, this operation is `PUT /Work_Orders/:recordId/actions/blueprint` (base URL `{{credentials.accessTokenRequest.api_domain}}/fsm/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/perform-work-order-transition.md) for the provider-specific parameters and requirements.

