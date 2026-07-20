# HelpCrunch: List Customers

Retrieves a list of customers from HelpCrunch.

```
GET https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpCrunch `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/list-customers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
      "device": {},
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
| `device` | object |  |
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

Through the native HelpCrunch API, this operation is `GET /customers` (base URL `https://api.helpcrunch.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

