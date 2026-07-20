# Front: List Contacts

Retrieves a list of contacts from Front.

```
GET https://connect.mindcloud.co/v1/universal/front/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Front `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/front/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/front/latest/actions/list-contacts?${params}`, {
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
      "account": {},
      "avatarUrl": {},
      "description": "string",
      "handles": [
        {
          "handle": "string",
          "source": "string"
        }
      ],
      "id": "string",
      "isPrivate": true,
      "links": {
        "related": {
          "conversations": "https://example.com",
          "notes": "https://example.com",
          "owner": {}
        },
        "self": "https://example.com"
      },
      "name": "Ava Chen",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `avatarUrl` | object |  |
| `description` | string |  |
| `handles[].handle` | string |  |
| `handles[].source` | string |  |
| `id` | string |  |
| `isPrivate` | boolean |  |
| `links.related.conversations` | string |  |
| `links.related.notes` | string |  |
| `links.related.owner` | object |  |
| `links.self` | string |  |
| `name` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Front API, this operation is `GET /contacts` (base URL `https://api2.frontapp.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

