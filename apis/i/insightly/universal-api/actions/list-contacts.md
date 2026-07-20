# Insightly: List Contacts

Retrieves a list of contacts from Insightly.

```
GET https://connect.mindcloud.co/v1/universal/insightly/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightly/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightly/latest/actions/list-contacts?${params}`, {
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
| `brief` | boolean | no | Return only top-level properties for each contact. |
| `countTotal` | boolean | no | Return the total-record count in the response headers. |

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

Through the native Insightly API, this operation is `GET {{credentials.apiBaseUrl}}Contacts` (base URL `https://api.na1.insightly.com/v3.1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

