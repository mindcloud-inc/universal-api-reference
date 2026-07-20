# Reteach: Get Customer



```
GET https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reteach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerIdentifier=2bf64377-4a26-4439-9c69-323b9111ea70" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerIdentifier": "2bf64377-4a26-4439-9c69-323b9111ea70"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-customer?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerIdentifier` | string | yes | The customer id, email, username, or externalId. Default: `2bf64377-4a26-4439-9c69-323b9111ea70`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticationMethod": "string",
      "birthDate": "string",
      "company": "string",
      "department": "string",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "expiredNotificationMail": "string",
      "externalId": "string",
      "firstName": "Ava",
      "gender": "string",
      "id": "string",
      "language": "string",
      "lastLoginAt": "string",
      "lastName": "Chen",
      "location": "string",
      "manager": {},
      "managerId": "string",
      "note": "string",
      "position": "string",
      "registeredAt": "string",
      "setActiveAt": "string",
      "setInactiveAt": "string",
      "source": "string",
      "status": "string",
      "tags": [
        {}
      ],
      "team": "string",
      "timezone": "string",
      "userName": "Ava Chen",
      "userType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticationMethod` | string |  |
| `birthDate` | string |  |
| `company` | string |  |
| `department` | string |  |
| `displayName` | string |  |
| `email` | string |  |
| `expiredNotificationMail` | string |  |
| `externalId` | string |  |
| `firstName` | string |  |
| `gender` | string |  |
| `id` | string |  |
| `language` | string |  |
| `lastLoginAt` | string |  |
| `lastName` | string |  |
| `location` | string |  |
| `manager` | object |  |
| `managerId` | string |  |
| `note` | string |  |
| `position` | string |  |
| `registeredAt` | string |  |
| `setActiveAt` | string |  |
| `setInactiveAt` | string |  |
| `source` | string |  |
| `status` | string |  |
| `tags` | array<object> |  |
| `team` | string |  |
| `timezone` | string |  |
| `userName` | string |  |
| `userType` | string |  |

## Native endpoint

Through the native Reteach API, this operation is `GET /customer/{customerIdentifier}` (base URL `https://api.reteach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

