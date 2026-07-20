# CompanyCam: Update User

Update an existing user in CompanyCam.

```
POST https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyCam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/update-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `emailAddress` | string | no |  |
| `phoneNumber` | string | no |  |
| `password` | string | no |  |
| `id` | string | yes | ID of the User |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "emailAddress": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "phoneNumber": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userRole": "string",
      "userUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string |  |
| `createdAt` | date |  |
| `emailAddress` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `phoneNumber` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `userRole` | string |  |
| `userUrl` | string |  |

## Native endpoint

Through the native CompanyCam API, this operation is `PUT users/:id` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

