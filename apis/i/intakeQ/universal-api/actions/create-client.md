# IntakeQ: Create Client

Creates a new client in IntakeQ.

```
POST https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/create-client', {
  method: 'POST',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "archived": true,
      "clientId": 1,
      "customFields": [
        {}
      ],
      "dateCreated": 1,
      "dateOfBirth": 1,
      "email": "ava@example.com",
      "externalClientId": "string",
      "firstName": "Ava",
      "lastName": "Chen",
      "lastUpdateDate": 1,
      "name": "Ava Chen",
      "phone": "string",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `archived` | boolean |  |
| `clientId` | number |  |
| `customFields` | array<object> |  |
| `dateCreated` | number |  |
| `dateOfBirth` | number |  |
| `email` | string |  |
| `externalClientId` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `lastUpdateDate` | number |  |
| `name` | string |  |
| `phone` | string |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native IntakeQ API, this operation is `POST /clients` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

