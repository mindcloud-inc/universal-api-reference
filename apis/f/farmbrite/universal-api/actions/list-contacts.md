# Farmbrite: List contacts

Retrieves a list of contacts from Farmbrite.

```
GET https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Farmbrite `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-contacts?${params}`, {
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
| `page` | number | no |  |
| `limit` | number | no |  |
| `sortBy` | string | no |  |
| `sortDir` | list | no | One of: `Ascending`, `Descending`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cached": true,
      "currentPage": 1,
      "data": [
        {
          "cell": "string",
          "company": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "doNotMail": true,
          "email": "ava@example.com",
          "fax": "string",
          "firstName": "Ava",
          "id": "string",
          "label": "string",
          "lastName": "Chen",
          "phone": "string",
          "taxExempt": true,
          "type": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "limit": 1,
      "message": "string",
      "success": true,
      "totalPages": 1,
      "totalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cached` | boolean |  |
| `currentPage` | number |  |
| `data` | array<object> |  |
| `data[].cell` | string |  |
| `data[].company` | string |  |
| `data[].createdAt` | date |  |
| `data[].description` | string |  |
| `data[].doNotMail` | boolean |  |
| `data[].email` | string |  |
| `data[].fax` | string |  |
| `data[].firstName` | string |  |
| `data[].id` | string |  |
| `data[].label` | string |  |
| `data[].lastName` | string |  |
| `data[].phone` | string |  |
| `data[].taxExempt` | boolean |  |
| `data[].type` | string |  |
| `data[].updatedAt` | date |  |
| `limit` | number |  |
| `message` | string |  |
| `success` | boolean |  |
| `totalPages` | number |  |
| `totalRecords` | number |  |

## Native endpoint

Through the native Farmbrite API, this operation is `GET /contacts` (base URL `https://api.farmbrite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

