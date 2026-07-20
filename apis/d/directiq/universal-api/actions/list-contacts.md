# DirectIQ: List Contacts

Retrieves a paginated list of contacts from DirectIQ.

```
GET https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-contacts?${params}`, {
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
      "clientId": 1,
      "createdDate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "keys": [
        [
          {}
        ]
      ],
      "lastName": "Chen",
      "lists": [
        [
          {}
        ]
      ],
      "notes": [
        [
          {}
        ]
      ],
      "quality": 1,
      "reactivationRequests": [
        [
          {}
        ]
      ],
      "status": "string",
      "statusDate": "2026-05-07T12:00:00.000Z",
      "tags": [
        [
          {}
        ]
      ],
      "updatedDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | number |  |
| `createdDate` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `keys[]` | array<object> |  |
| `keys[].dateFormat` | string |  |
| `keys[].dateValue` | date |  |
| `keys[].id` | number |  |
| `keys[].keyType` | number |  |
| `keys[].name` | string |  |
| `keys[].numberValue` | number |  |
| `keys[].shortCode` | string |  |
| `keys[].value` | string |  |
| `lastName` | string |  |
| `lists[]` | array<object> |  |
| `lists[].id` | number |  |
| `lists[].name` | string |  |
| `notes[]` | array<object> |  |
| `notes[].createdDate` | date |  |
| `notes[].id` | number |  |
| `notes[].note` | string |  |
| `quality` | number |  |
| `reactivationRequests[]` | array<object> |  |
| `status` | string |  |
| `statusDate` | date |  |
| `tags[]` | array<object> |  |
| `tags[].id` | number |  |
| `tags[].name` | string |  |
| `updatedDate` | date |  |

## Native endpoint

Through the native DirectIQ API, this operation is `GET /contacts/contact/list` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

