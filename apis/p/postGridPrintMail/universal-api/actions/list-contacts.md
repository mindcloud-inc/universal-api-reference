# PostGrid Print & Mail: List Contacts

Retrieves contacts from PostGrid Print & Mail.

```
GET https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostGrid Print & Mail `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/list-contacts?${params}`, {
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
| `search` | string | no | Filter results by a free-text search string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressLine1": "string",
      "addressStatus": "string",
      "city": "string",
      "country": "string",
      "countryCode": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "live": true,
      "mailingLists": [
        {}
      ],
      "object": "string",
      "postalOrZip": "string",
      "provinceOrState": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressLine1` | string |  |
| `addressStatus` | string |  |
| `city` | string |  |
| `country` | string |  |
| `countryCode` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `live` | boolean |  |
| `mailingLists` | array<object> |  |
| `object` | string |  |
| `postalOrZip` | string |  |
| `provinceOrState` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native PostGrid Print & Mail API, this operation is `GET /contacts` (base URL `https://api.postgrid.com/print-mail/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

