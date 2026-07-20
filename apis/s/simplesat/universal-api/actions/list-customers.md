# Simplesat: List Customers

Retrieves customers from Simplesat.

```
GET https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplesat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/list-customers?${params}`, {
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
| `page` | number | no | The page number to retrieve |
| `pageSize` | number | no | The number of records per page |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdAfter` | string | no | Filter customers created after this date (ISO 8601 format) |
| `createdBefore` | string | no | Filter customers created before this date (ISO 8601 format) |
| `modifiedAfter` | string | no | Filter customers modified after this date (ISO 8601 format) |
| `modifiedBefore` | string | no | Filter customers modified before this date (ISO 8601 format) |
| `subscribed` | boolean | no | Filter customers by subscription status |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "created": "string",
      "custom_attributes": {},
      "email": "ava@example.com",
      "external_id": "string",
      "id": 1,
      "modified": "string",
      "name": "Ava Chen",
      "subscribed": true,
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
| `company` | string |  |
| `created` | string |  |
| `custom_attributes` | object |  |
| `email` | string |  |
| `external_id` | string |  |
| `id` | number |  |
| `modified` | string |  |
| `name` | string |  |
| `subscribed` | boolean |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native Simplesat API, this operation is `GET /api/v1/customers` (base URL `https://api.simplesat.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

