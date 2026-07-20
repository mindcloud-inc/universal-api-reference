# DirectIQ: Search Contacts

Finds contacts in DirectIQ created after a given date.

```
GET https://connect.mindcloud.co/v1/universal/directiq/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/search-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directiq/latest/actions/search-contacts?${params}`, {
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
      "contacts": [
        [
          {}
        ]
      ],
      "nextPageToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts[]` | array<object> |  |
| `contacts[].clientId` | number |  |
| `contacts[].createdDate` | date |  |
| `contacts[].email` | string |  |
| `contacts[].firstName` | string |  |
| `contacts[].id` | number |  |
| `contacts[].keys[]` | array<object> |  |
| `contacts[].keys[].dateFormat` | string |  |
| `contacts[].keys[].dateValue` | date |  |
| `contacts[].keys[].id` | number |  |
| `contacts[].keys[].keyType` | number |  |
| `contacts[].keys[].name` | string |  |
| `contacts[].keys[].numberValue` | number |  |
| `contacts[].keys[].shortCode` | string |  |
| `contacts[].keys[].value` | string |  |
| `contacts[].lastName` | string |  |
| `contacts[].lists[]` | array<object> |  |
| `contacts[].lists[].id` | number |  |
| `contacts[].lists[].name` | string |  |
| `contacts[].notes[]` | array<object> |  |
| `contacts[].notes[].createdDate` | date |  |
| `contacts[].notes[].id` | number |  |
| `contacts[].notes[].note` | string |  |
| `contacts[].quality` | number |  |
| `contacts[].reactivationRequests[]` | array<object> |  |
| `contacts[].reactivationRequests[].active` | boolean |  |
| `contacts[].reactivationRequests[].completedDate` | date |  |
| `contacts[].reactivationRequests[].createdDate` | date |  |
| `contacts[].reactivationRequests[].hashId` | string |  |
| `contacts[].reactivationRequests[].language` | string |  |
| `contacts[].reactivationRequests[].s3Key` | string |  |
| `contacts[].status` | string |  |
| `contacts[].statusDate` | date |  |
| `contacts[].tags[]` | array<object> |  |
| `contacts[].tags[].id` | number |  |
| `contacts[].tags[].name` | string |  |
| `contacts[].updatedDate` | date |  |
| `nextPageToken` | string |  |

## Native endpoint

Through the native DirectIQ API, this operation is `GET /contacts/contact/filter` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

