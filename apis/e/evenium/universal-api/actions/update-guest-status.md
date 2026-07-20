# Evenium: Update Guest Status

Updates a guest status in Evenium.

```
PUT https://connect.mindcloud.co/v1/universal/evenium/latest/actions/update-guest-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evenium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/evenium/latest/actions/update-guest-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evenium/latest/actions/update-guest-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | no | The Evenium contact ID. |
| `eventId` | string | no | The Evenium event ID. |
| `status` | string | no | The new guest status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": 1,
      "eventId": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | number | Guest contact ID. |
| `eventId` | number | Parent event ID. |
| `status` | string | Guest status value. |

## Native endpoint

Through the native Evenium API, this operation is `PUT /events/:eventId/guests/:contactId/status` (base URL `https://evenium.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-guest-status.md) for the provider-specific parameters and requirements.

