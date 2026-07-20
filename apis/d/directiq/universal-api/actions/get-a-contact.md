# DirectIQ: Get a contact

Retrieves a contact from DirectIQ by ID.

```
GET https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-a-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-a-contact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-a-contact?${params}`, {
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
| `reactivationRequests[].active` | boolean |  |
| `reactivationRequests[].completedDate` | date |  |
| `reactivationRequests[].createdDate` | date |  |
| `reactivationRequests[].hashId` | string |  |
| `reactivationRequests[].language` | string |  |
| `reactivationRequests[].s3Key` | string |  |
| `status` | string |  |
| `statusDate` | date |  |
| `tags[]` | array<object> |  |
| `tags[].id` | number |  |
| `tags[].name` | string |  |
| `updatedDate` | date |  |

## Native endpoint

Through the native DirectIQ API, this operation is `GET /contacts/contact/get/{id}` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-contact.md) for the provider-specific parameters and requirements.

