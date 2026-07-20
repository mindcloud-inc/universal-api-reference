# Insightly: Get Contact

Retrieves a contact from Insightly by ID.

```
GET https://connect.mindcloud.co/v1/universal/insightly/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightly/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightly/latest/actions/get-contact?${params}`, {
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
| `contactId` | number | yes | The Contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": 1,
      "createdUserId": 1,
      "dateCreatedUtc": "2026-05-07T12:00:00.000Z",
      "dateUpdatedUtc": "2026-05-07T12:00:00.000Z",
      "emailAddress": "ava@example.com",
      "emailOptedOut": true,
      "firstName": "Ava",
      "imageUrl": "https://example.com",
      "lastActivityDateUtc": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "nextActivityDateUtc": "2026-05-07T12:00:00.000Z",
      "organisationId": 1,
      "ownerUserId": 1,
      "phone": "string",
      "title": "string",
      "visibleTo": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | number |  |
| `createdUserId` | number |  |
| `dateCreatedUtc` | date |  |
| `dateUpdatedUtc` | date |  |
| `emailAddress` | string |  |
| `emailOptedOut` | boolean |  |
| `firstName` | string |  |
| `imageUrl` | string |  |
| `lastActivityDateUtc` | date |  |
| `lastName` | string |  |
| `nextActivityDateUtc` | date |  |
| `organisationId` | number |  |
| `ownerUserId` | number |  |
| `phone` | string |  |
| `title` | string |  |
| `visibleTo` | string |  |

## Native endpoint

Through the native Insightly API, this operation is `GET {{credentials.apiBaseUrl}}Contacts/:contactId` (base URL `https://api.na1.insightly.com/v3.1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

