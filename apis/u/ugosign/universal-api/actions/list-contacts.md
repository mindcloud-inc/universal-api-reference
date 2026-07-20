# Ugosign: List Contacts

Retrieves contacts from Ugosign.

```
GET https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ugosign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/list-contacts?${params}`, {
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
      "address": {
        "city": "string",
        "country": "string",
        "postalCode": "string",
        "street": "string",
        "street2": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "familyName": "Ava Chen",
      "gender": "string",
      "givenName": "Ava Chen",
      "id": "string",
      "phoneNumber": "string",
      "position": "string",
      "privateComment": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.city` | string |  |
| `address.country` | string |  |
| `address.postalCode` | string |  |
| `address.street` | string |  |
| `address.street2` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `familyName` | string |  |
| `gender` | string |  |
| `givenName` | string |  |
| `id` | string |  |
| `phoneNumber` | string |  |
| `position` | string |  |
| `privateComment` | string |  |
| `updatedAt` | date |  |
| `website` | string |  |

## Native endpoint

Through the native Ugosign API, this operation is `GET /v1/contacts` (base URL `https://app.ugosign.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

