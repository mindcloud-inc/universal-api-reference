# HelpSpace: List Customers

Retrieves customers from HelpSpace.

```
GET https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpSpace `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-customers?${params}`, {
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
      "address": "string",
      "city": "string",
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": {},
      "email": "ava@example.com",
      "id": 1,
      "jobTitle": "string",
      "locale": "string",
      "name": "Ava Chen",
      "note": "string",
      "postalCode": "string",
      "state": "string",
      "timezone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `city` | string |  |
| `country` | string |  |
| `createdAt` | date |  |
| `customFields` | object |  |
| `email` | string |  |
| `id` | number |  |
| `jobTitle` | string |  |
| `locale` | string |  |
| `name` | string |  |
| `note` | string |  |
| `postalCode` | string |  |
| `state` | string |  |
| `timezone` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native HelpSpace API, this operation is `GET /customers` (base URL `https://api.helpspace.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

