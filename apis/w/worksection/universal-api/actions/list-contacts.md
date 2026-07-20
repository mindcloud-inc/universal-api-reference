# Worksection: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/worksection/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksection `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worksection/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worksection/latest/actions/list-contacts?${params}`, {
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
      "dateAdded": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "group": "string",
      "id": "string",
      "lastName": "Chen",
      "name": "Ava Chen",
      "phone": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateAdded` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `group` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Worksection API, this operation is `GET /` (base URL `https://min7657.worksection.com/api/admin/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

