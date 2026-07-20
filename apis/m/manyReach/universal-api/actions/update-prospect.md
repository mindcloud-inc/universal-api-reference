# ManyReach: Update Prospect

Updates an existing prospect in ManyReach.

```
PUT https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/update-prospect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/update-prospect" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/update-prospect', {
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
| `firstName` | string | no | Updated prospect first name. |
| `id` | string | no | Prospect ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseListId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "notes": "string",
      "prospectId": 1,
      "sendingActive": true,
      "sendingStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseListId` | number |  |
| `createdAt` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `notes` | string |  |
| `prospectId` | number |  |
| `sendingActive` | boolean |  |
| `sendingStatus` | string |  |

## Native endpoint

Through the native ManyReach API, this operation is `PATCH https://api.manyreach.com/api/v2/prospects/:id` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-prospect.md) for the provider-specific parameters and requirements.

