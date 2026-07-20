# Ascora: List Quotes

Retrieves quotes from Ascora.

```
GET https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-quotes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-quotes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-quotes?${params}`, {
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
| `assignedUser` | string | no | Filter by the full name of the assigned user. |
| `customerName` | string | no | Partial match against the site or billing customer name. |
| `filterText` | string | no | Partial match against quote number, name, or address. |
| `jobType` | string | no | Filter by related job type name. |
| `quoteStatus` | string | no | Quote status such as IN-PROGRESS, SENT-TO-CUSTOMER, OPEN, WON, LAST-7-DAYS, ALL, or ACCEPTED. |
| `startDate` | date | no | Filter for quotes created on or after this date. |
| `endDate` | date | no | Filter for quotes created on or before this date. |
| `pageSize` | number | no | Result page size. Ascora defaults to 250 when omitted. |
| `page` | number | no | Page number to retrieve. Ascora defaults to page 1 when omitted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {}
      ],
      "success": true,
      "totalPages": 1,
      "totalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> | Matching quote records. |
| `success` | boolean | Whether Ascora returned the quotes search successfully. |
| `totalPages` | number | Total result pages returned by Ascora. |
| `totalRecords` | number | Total matching quotes. |

## Native endpoint

Through the native Ascora API, this operation is `GET /Quotes/Quotes` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-quotes.md) for the provider-specific parameters and requirements.

