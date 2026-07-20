# HelpCrunch: Get Customer

Retrieves a single customer from HelpCrunch.

```
GET https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpCrunch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/get-customer?${params}`, {
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
| `customerId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blocked": true,
      "company": "string",
      "createdFrom": "string",
      "customData": [
        {}
      ],
      "device": "string",
      "email": "ava@example.com",
      "firstSeen": "string",
      "id": 1,
      "integrationId": "string",
      "lastPage": "string",
      "lastSeen": "string",
      "locale": "string",
      "location": {},
      "name": "Ava Chen",
      "notes": "string",
      "phone": "string",
      "referer": "string",
      "source": "string",
      "tags": [
        {}
      ],
      "unsubscribed": true,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocked` | boolean |  |
| `company` | string |  |
| `createdFrom` | string |  |
| `customData` | array<object> |  |
| `device` | string |  |
| `email` | string |  |
| `firstSeen` | string |  |
| `id` | number |  |
| `integrationId` | string |  |
| `lastPage` | string |  |
| `lastSeen` | string |  |
| `locale` | string |  |
| `location` | object |  |
| `name` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `referer` | string |  |
| `source` | string |  |
| `tags` | array<object> |  |
| `unsubscribed` | boolean |  |
| `userId` | string |  |

## Native endpoint

Through the native HelpCrunch API, this operation is `GET /customers/:customerId` (base URL `https://api.helpcrunch.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

