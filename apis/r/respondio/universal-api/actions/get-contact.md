# respond.io: Get Contact

Retrieves a contact from respond.io.

```
GET https://connect.mindcloud.co/v1/universal/respondio/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a respond.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/respondio/latest/actions/get-contact?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/respondio/latest/actions/get-contact?${params}`, {
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
| `identifier` | string | yes | Contact identifier (id:, email:, or phone:). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee": {},
      "countryCode": "string",
      "createdAt": 1,
      "customFields": {},
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "isBlocked": true,
      "language": "string",
      "lastName": "Chen",
      "lifecycle": "string",
      "locale": "string",
      "phone": "string",
      "profilePic": "string",
      "status": "string",
      "tags": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee` | object |  |
| `countryCode` | string |  |
| `createdAt` | number |  |
| `customFields` | object |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `isBlocked` | boolean |  |
| `language` | string |  |
| `lastName` | string |  |
| `lifecycle` | string |  |
| `locale` | string |  |
| `phone` | string |  |
| `profilePic` | string |  |
| `status` | string |  |
| `tags` | object |  |

## Native endpoint

Through the native respond.io API, this operation is `GET /contact/:identifier` (base URL `https://api.respond.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

