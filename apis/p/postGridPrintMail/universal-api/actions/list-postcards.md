# PostGrid Print & Mail: List Postcards

Retrieves postcards from PostGrid Print & Mail.

```
GET https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/list-postcards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostGrid Print & Mail `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/list-postcards?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/list-postcards?${params}`, {
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
      "backHTML": "string",
      "cancellation": {},
      "carrierTracking": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "frontHTML": "string",
      "id": "string",
      "live": true,
      "mailingClass": "string",
      "object": "string",
      "pageCount": 1,
      "paper": "string",
      "sendDate": "2026-05-07T12:00:00.000Z",
      "size": "string",
      "status": "string",
      "to": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backHTML` | string |  |
| `cancellation` | object |  |
| `carrierTracking` | object |  |
| `createdAt` | date |  |
| `description` | string |  |
| `frontHTML` | string |  |
| `id` | string |  |
| `live` | boolean |  |
| `mailingClass` | string |  |
| `object` | string |  |
| `pageCount` | number |  |
| `paper` | string |  |
| `sendDate` | date |  |
| `size` | string |  |
| `status` | string |  |
| `to` | object |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native PostGrid Print & Mail API, this operation is `GET /postcards` (base URL `https://api.postgrid.com/print-mail/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-postcards.md) for the provider-specific parameters and requirements.

