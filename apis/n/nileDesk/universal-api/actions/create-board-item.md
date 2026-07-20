# NileDesk: Create Board Item

Creates a live board item in NileDesk.

```
POST https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/create-board-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NileDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/create-board-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "step_id": "string",
  "template_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/create-board-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "step_id": "string",
    "template_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `form_fields` | object | no | Optional board form field values keyed by NileDesk field identifier. |
| `form_tables` | object | no | Optional embedded table payload keyed by collection name. |
| `step_id` | string | yes | The target board drop step identifier. |
| `template_id` | string | yes | The NileDesk board template to initiate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider message describing the result. |
| `success` | boolean | Whether NileDesk accepted the request. |

## Native endpoint

Through the native NileDesk API, this operation is `POST /InitiateBoardItem` (base URL `https://app.niledesk.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-board-item.md) for the provider-specific parameters and requirements.

