# Starfish: List Contacts

Retrieves a list of contacts from Starfish.

```
GET https://connect.mindcloud.co/v1/universal/starfish/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starfish `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starfish/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starfish/latest/actions/list-contacts?${params}`, {
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
      "address": "string",
      "addressNumber": "string",
      "adminId": 1,
      "birthday": "2026-05-07T12:00:00.000Z",
      "chainId": 1,
      "city": "string",
      "company": "string",
      "contactId": 1,
      "contactUid": "string",
      "country": "string",
      "countryOrigin": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "gender": "string",
      "id": 1,
      "idIssueCountry": "string",
      "idNr": "string",
      "idType": "string",
      "invoices": [
        {}
      ],
      "lastModified": "2026-05-07T12:00:00.000Z",
      "lastModifiedSearch": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "location": [
        {}
      ],
      "meta": [
        {}
      ],
      "name": "Ava Chen",
      "nationality": "string",
      "phone": "string",
      "phoneMobile": "string",
      "reservations": [
        {}
      ],
      "state": "string",
      "status": "string",
      "type": "string",
      "vatNumber": "string",
      "zipcode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `addressNumber` | string |  |
| `adminId` | number |  |
| `birthday` | date |  |
| `chainId` | number |  |
| `city` | string |  |
| `company` | string |  |
| `contactId` | number |  |
| `contactUid` | string |  |
| `country` | string |  |
| `countryOrigin` | string |  |
| `created` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `gender` | string |  |
| `id` | number |  |
| `idIssueCountry` | string |  |
| `idNr` | string |  |
| `idType` | string |  |
| `invoices` | array<object> |  |
| `lastModified` | date |  |
| `lastModifiedSearch` | date |  |
| `lastName` | string |  |
| `location` | array<object> |  |
| `meta` | array<object> |  |
| `name` | string |  |
| `nationality` | string |  |
| `phone` | string |  |
| `phoneMobile` | string |  |
| `reservations` | array<object> |  |
| `state` | string |  |
| `status` | string |  |
| `type` | string |  |
| `vatNumber` | string |  |
| `zipcode` | string |  |

## Native endpoint

Through the native Starfish API, this operation is `GET /contacts` (base URL `https://api.camping.care/v21`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

