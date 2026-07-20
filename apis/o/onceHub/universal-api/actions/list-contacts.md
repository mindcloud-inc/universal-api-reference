# OnceHub: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnceHub `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/list-contacts?${params}`, {
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
      "bot": {},
      "city": {},
      "company": {},
      "companySize": {},
      "country": {},
      "creationTime": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "employees": {},
      "firstName": "Ava",
      "form": {},
      "hasConsent": true,
      "id": "string",
      "jobTitle": {},
      "lastInteractedTime": {},
      "lastName": {},
      "lastUpdatedTime": "2026-05-07T12:00:00.000Z",
      "mobilePhone": "string",
      "object": "string",
      "owner": "string",
      "phone": {},
      "postCode": {},
      "salutation": {},
      "state": {},
      "status": {},
      "streetAddress": {},
      "termsOfService": true,
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bot` | object |  |
| `city` | object |  |
| `company` | object |  |
| `companySize` | object |  |
| `country` | object |  |
| `creationTime` | date |  |
| `email` | string |  |
| `employees` | object |  |
| `firstName` | string |  |
| `form` | object |  |
| `hasConsent` | boolean |  |
| `id` | string |  |
| `jobTitle` | object |  |
| `lastInteractedTime` | object |  |
| `lastName` | object |  |
| `lastUpdatedTime` | date |  |
| `mobilePhone` | string |  |
| `object` | string |  |
| `owner` | string |  |
| `phone` | object |  |
| `postCode` | object |  |
| `salutation` | object |  |
| `state` | object |  |
| `status` | object |  |
| `streetAddress` | object |  |
| `termsOfService` | boolean |  |
| `timezone` | string |  |

## Native endpoint

Through the native OnceHub API, this operation is `GET /v2/contacts` (base URL `https://api.oncehub.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

