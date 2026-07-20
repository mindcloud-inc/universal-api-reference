# Open Letter Connect: List Contacts

Retrieves contacts from Open Letter Connect.

```
GET https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Letter Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/list-contacts?${params}`, {
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
      "address1": "string",
      "address2": "string",
      "addressStatus": "string",
      "city": "string",
      "companyName": "Ava Chen",
      "ContactLabels": [
        {
          "id": "string",
          "title": "string"
        }
      ],
      "createdAt": "string",
      "email": "ava@example.com",
      "extension": "string",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": "string",
      "isLiveMode": true,
      "isVerified": true,
      "lastMailedDate": "string",
      "lastMailedStatus": "string",
      "lastName": "Chen",
      "orgId": "string",
      "phoneNo": "string",
      "state": "string",
      "websiteUrl": "https://example.com",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address1` | string |  |
| `address2` | string |  |
| `addressStatus` | string |  |
| `city` | string |  |
| `companyName` | string |  |
| `ContactLabels[].id` | string |  |
| `ContactLabels[].title` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `extension` | string |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `isLiveMode` | boolean |  |
| `isVerified` | boolean |  |
| `lastMailedDate` | string |  |
| `lastMailedStatus` | string |  |
| `lastName` | string |  |
| `orgId` | string |  |
| `phoneNo` | string |  |
| `state` | string |  |
| `websiteUrl` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native Open Letter Connect API, this operation is `GET /contacts` (base URL `https://api.openletterconnect.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

