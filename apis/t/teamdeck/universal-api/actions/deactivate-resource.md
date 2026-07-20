# Teamdeck: Deactivate Resource

Deactivates an existing resource in Teamdeck.

```
PUT https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/deactivate-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamdeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/deactivate-resource" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/deactivate-resource', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The Teamdeck resource ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "avatar": "string",
      "canSeeCalendar": true,
      "contractEndDate": "string",
      "contractStartDate": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "id": 1,
      "isPartTime": true,
      "isVisible": true,
      "name": "Ava Chen",
      "organizationUnitId": 1,
      "role": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `avatar` | string |  |
| `canSeeCalendar` | boolean |  |
| `contractEndDate` | string |  |
| `contractStartDate` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `id` | number |  |
| `isPartTime` | boolean |  |
| `isVisible` | boolean |  |
| `name` | string |  |
| `organizationUnitId` | number |  |
| `role` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Teamdeck API, this operation is `PUT /resources/:id/deactivate` (base URL `https://api.teamdeck.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/deactivate-resource.md) for the provider-specific parameters and requirements.

