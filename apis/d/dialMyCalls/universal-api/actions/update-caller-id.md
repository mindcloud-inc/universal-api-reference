# DialMyCalls: Update Caller ID

Updates an existing caller ID in DialMyCalls.

```
PUT https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/update-caller-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DialMyCalls `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/update-caller-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "calleridId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/update-caller-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "calleridId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `calleridId` | string | yes | The DialMyCalls caller ID to update. |
| `name` | string | yes | The caller ID's name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approved": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "phone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approved` | boolean | Whether the caller ID is approved. |
| `createdAt` | date | When the caller ID was created. |
| `id` | string | Caller ID ID. |
| `name` | string | Caller ID label. |
| `phone` | string | Phone number. |
| `updatedAt` | date | When the caller ID was last updated. |

## Native endpoint

Through the native DialMyCalls API, this operation is `PUT /callerid/:CalleridId` (base URL `https://{{credentials.apiKey}}@api.dialmycalls.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-caller-id.md) for the provider-specific parameters and requirements.

