# NobelSMS: List Contacts

Retrieves contacts from NobelSMS.

```
GET https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NobelSMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/list-contacts?${params}`, {
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
| `blacklisted` | number | no | Blacklist flag. |
| `firstName` | string | no | First name. |
| `lastName` | string | no | Last name. |
| `phone` | string | no | Phone number. |
| `tagIds` | string | no | Comma-separated list of tag IDs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blacklisted": 1,
      "comments": "string",
      "first_name": "Ava",
      "id": 1,
      "last_name": "Chen",
      "phone": "string",
      "tag_ids": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blacklisted` | number |  |
| `comments` | string |  |
| `first_name` | string |  |
| `id` | number |  |
| `last_name` | string |  |
| `phone` | string |  |
| `tag_ids` | string |  |

## Native endpoint

Through the native NobelSMS API, this operation is `GET /contact` (base URL `https://api.nobelsms.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

