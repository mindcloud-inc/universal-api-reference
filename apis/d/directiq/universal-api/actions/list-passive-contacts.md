# DirectIQ: List Passive Contacts

Retrieves a paginated list of passive contacts from DirectIQ.

```
GET https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-passive-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-passive-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directiq/latest/actions/list-passive-contacts?${params}`, {
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
| `contacts[].createdDate` | date |  |
| `contacts[].email` | string |  |
| `contacts[].firstName` | string |  |
| `contacts[].id` | number |  |
| `contacts[].lastName` | string |  |
| `contacts[].status` | string |  |
| `nextPageToken` | string |  |

## Native endpoint

Through the native DirectIQ API, this operation is `GET /contacts/contact/passive` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-passive-contacts.md) for the provider-specific parameters and requirements.

