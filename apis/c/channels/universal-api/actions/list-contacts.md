# Channels: List Contacts

Retrieves contacts from Channels.

```
GET https://connect.mindcloud.co/v1/universal/channels/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channels `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channels/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channels/latest/actions/list-contacts?${params}`, {
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
| `modificationDateFrom` | string | no | Optional lower bound for contact last modification date. |
| `orderModificationDate` | string | no | Optional sort direction for contact last modification date; docs allow asc or desc. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `msisdn` | string | no | Optional filter for contacts whose MSISDN contains the provided sequence. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "alternativeMsisdns": [
            "string"
          ],
          "company": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "email": "ava@example.com",
          "externalLink": "https://example.com",
          "externalOrderLink": "https://example.com",
          "externalServices": {
            "recordId": 1
          },
          "firstName": "Ava",
          "id": 1,
          "lastModificationDate": "2026-05-07T12:00:00.000Z",
          "lastName": "Chen",
          "source": "string"
        }
      ],
      "links": {
        "first": "https://example.com",
        "last": "https://example.com",
        "next": "https://example.com",
        "prev": "https://example.com"
      },
      "total": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].alternativeMsisdns[]` | string |  |
| `data[].company` | string |  |
| `data[].createdAt` | date |  |
| `data[].email` | string |  |
| `data[].externalLink` | string |  |
| `data[].externalOrderLink` | string |  |
| `data[].externalServices.recordId` | number |  |
| `data[].firstName` | string |  |
| `data[].id` | number |  |
| `data[].lastModificationDate` | date |  |
| `data[].lastName` | string |  |
| `data[].source` | string |  |
| `links.first` | string |  |
| `links.last` | string |  |
| `links.next` | string |  |
| `links.prev` | string |  |
| `total` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Channels API, this operation is `GET /api/v1/contacts` (base URL `https://api.channels.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

