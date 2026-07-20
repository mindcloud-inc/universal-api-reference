# Rentman: List Contact Persons



```
GET https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-contact-persons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rentman `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-contact-persons?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-contact-persons?${params}`, {
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
| `id` | number | yes | Numeric Rentman contact identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "contact": "string",
      "country": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "custom": {},
      "displayname": "Ava Chen",
      "email": "ava@example.com",
      "firstname": "Ava",
      "function": "string",
      "id": 1,
      "lastname": "Chen",
      "middle_name": "Ava Chen",
      "mobilephone": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "number": "string",
      "phone": "string",
      "postalcode": "string",
      "state": "string",
      "street": "string",
      "tags": "string",
      "updateHash": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `contact` | string |  |
| `country` | string |  |
| `created` | date |  |
| `custom` | object |  |
| `displayname` | string |  |
| `email` | string |  |
| `firstname` | string |  |
| `function` | string |  |
| `id` | number |  |
| `lastname` | string |  |
| `middle_name` | string |  |
| `mobilephone` | string |  |
| `modified` | date |  |
| `number` | string |  |
| `phone` | string |  |
| `postalcode` | string |  |
| `state` | string |  |
| `street` | string |  |
| `tags` | string |  |
| `updateHash` | string |  |

## Native endpoint

Through the native Rentman API, this operation is `GET /contacts/:id/contactpersons` (base URL `https://api.rentman.net`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contact-persons.md) for the provider-specific parameters and requirements.

