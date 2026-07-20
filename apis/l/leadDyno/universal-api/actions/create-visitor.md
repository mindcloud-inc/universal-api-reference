# LeadDyno: Create Visitor

Creates a new visitor in LeadDyno.

```
POST https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/create-visitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadDyno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/create-visitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tracking_code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/create-visitor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tracking_code": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tracking_code` | string | yes | The tracking code assigned to the visitor. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliate": {},
      "campaign": {},
      "created_at": "string",
      "id": 1,
      "latest_click": "string",
      "lead": {},
      "tracking_code": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliate` | object |  |
| `campaign` | object |  |
| `created_at` | string |  |
| `id` | number |  |
| `latest_click` | string |  |
| `lead` | object |  |
| `tracking_code` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native LeadDyno API, this operation is `POST /visitors` (base URL `https://api.leaddyno.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-visitor.md) for the provider-specific parameters and requirements.

