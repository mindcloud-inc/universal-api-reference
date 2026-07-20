# Quo: List Phone Numbers

Retrieves all phone numbers from Quo.

```
GET https://connect.mindcloud.co/v1/universal/quo/latest/actions/list-phone-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quo/latest/actions/list-phone-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quo/latest/actions/list-phone-numbers?${params}`, {
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
| `userId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "formattedNumber": "string",
      "forward": {},
      "groupId": "string",
      "id": "string",
      "name": "Ava Chen",
      "number": "string",
      "portingStatus": {},
      "portRequestId": {},
      "restrictions": {
        "calling": {
          "ca": "string",
          "intl": "string",
          "us": "string"
        },
        "messaging": {
          "ca": "string",
          "intl": "string",
          "us": "string"
        }
      },
      "symbol": "string",
      "updatedAt": "string",
      "users": [
        {
          "email": "ava@example.com",
          "firstName": "Ava",
          "groupId": "string",
          "id": "string",
          "lastName": "Chen",
          "role": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `formattedNumber` | string |  |
| `forward` | object |  |
| `groupId` | string |  |
| `id` | string |  |
| `name` | string |  |
| `number` | string |  |
| `portingStatus` | object |  |
| `portRequestId` | object |  |
| `restrictions.calling.ca` | string |  |
| `restrictions.calling.intl` | string |  |
| `restrictions.calling.us` | string |  |
| `restrictions.messaging.ca` | string |  |
| `restrictions.messaging.intl` | string |  |
| `restrictions.messaging.us` | string |  |
| `symbol` | string |  |
| `updatedAt` | string |  |
| `users[].email` | string |  |
| `users[].firstName` | string |  |
| `users[].groupId` | string |  |
| `users[].id` | string |  |
| `users[].lastName` | string |  |
| `users[].role` | string |  |

## Native endpoint

Through the native Quo API, this operation is `GET /phone-numbers` (base URL `https://api.openphone.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-phone-numbers.md) for the provider-specific parameters and requirements.

