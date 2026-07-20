# KleverKey: Manage Bookings



```
POST https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/manage-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KleverKey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/manage-bookings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": 1,
  "serviceName": "Ava Chen",
  "operationType": 1,
  "permission.lockIds": "string",
  "permission.referenceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/manage-bookings', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": 1,
    "serviceName": "Ava Chen",
    "operationType": 1,
    "permission.lockIds": "string",
    "permission.referenceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | number | yes |  |
| `serviceName` | string | yes |  |
| `operationType` | number | yes | 1 = CreateOrUpdate, 2 = Delete |
| `userEmail` | string | no | Email for the booking user. |
| `userName` | string | no | Display name for the booking user. |
| `permission.lockIds` | string | yes | Comma separated list of lock IDs |
| `permission.referenceId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invitations": [
        {}
      ],
      "lockActivationLinks": [
        {}
      ],
      "permissions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invitations` | array<object> |  |
| `lockActivationLinks` | array<object> |  |
| `permissions` | array<object> |  |

## Native endpoint

Through the native KleverKey API, this operation is `POST /api/v1/organizations/:organizationId/bookings/:serviceName` (base URL `https://api.kleverkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/manage-bookings.md) for the provider-specific parameters and requirements.

