# OnceHub: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnceHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/get-contact?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The OnceHub contact identifier. |

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

Through the native OnceHub API, this operation is `GET /v2/contacts/:id` (base URL `https://api.oncehub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

