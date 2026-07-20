# Open Letter Connect: Create Contact

Creates a contact in Open Letter Connect.

```
POST https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Letter Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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

Through the native Open Letter Connect API, this operation is `POST /contacts` (base URL `https://api.openletterconnect.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

