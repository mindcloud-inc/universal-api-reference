# pretix: List Invoices

Retrieves invoices from a pretix event.

```
GET https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pretix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0&organizer=string&event=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizer": "string",
  "event": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-invoices?${params}`, {
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
| `organizer` | string | yes | pretix organizer slug. |
| `event` | string | yes | pretix event slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "datetime": "string",
      "event": "string",
      "invoiceFrom": "string",
      "invoiceFromCity": "string",
      "invoiceFromCountry": "string",
      "invoiceFromName": "Ava Chen",
      "invoiceFromZipcode": "string",
      "invoiceToName": "Ava Chen",
      "isCancellation": true,
      "number": "string",
      "order": "string",
      "total": "string",
      "transmissionType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `datetime` | string |  |
| `event` | string |  |
| `invoiceFrom` | string |  |
| `invoiceFromCity` | string |  |
| `invoiceFromCountry` | string |  |
| `invoiceFromName` | string |  |
| `invoiceFromZipcode` | string |  |
| `invoiceToName` | string |  |
| `isCancellation` | boolean |  |
| `number` | string |  |
| `order` | string |  |
| `total` | string |  |
| `transmissionType` | string |  |

## Native endpoint

Through the native pretix API, this operation is `GET /organizers/:organizer/events/:event/invoices/` (base URL `https://pretix.eu/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

