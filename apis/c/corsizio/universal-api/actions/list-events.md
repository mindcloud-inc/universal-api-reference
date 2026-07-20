# Corsizio: List Events

Retrieves events from a Corsizio account.

```
GET https://connect.mindcloud.co/v1/universal/corsizio/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Corsizio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/corsizio/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/corsizio/latest/actions/list-events?${params}`, {
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
| `order` | list<string> | no | Sort order such as startDate, endDate, created, or -endDate. One of: `-created`, `-endDate`, `-startDate`, `created`, `endDate`, `startDate`. |
| `status` | list<string> | no | Event status filter such as published, draft, archived, deleted, or any. One of: `any`, `archived`, `deleted`, `draft`, `published`. |
| `date` | string | no | Date range like 2026-03-01:2026-03-31. |
| `price` | string | no | Price range like 50:200 or :300. |
| `category` | string | no | Filter by a category ID from Corsizio account setup. |
| `location` | string | no | Filter by a location ID from Corsizio account setup. |
| `age` | string | no | Filter by an age group ID from Corsizio account setup. |
| `gender` | string | no | Filter by a gender ID from Corsizio account setup. |
| `level` | string | no | Filter by a level ID from Corsizio account setup. |
| `search` | string | no | Search by event name or exact event ID. |
| `include` | list<string> | no | Comma-separated values: details, filters, stats, config. One of: `config`, `details`, `filters`, `stats`. Accepts multiple values in one string, delimited by `,`. |
| `expand` | list<string> | no | Comma-separated values: filters, instructors, account. One of: `account`, `filters`, `instructors`. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "displayDate": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "formUrl": "https://example.com",
      "hideDates": true,
      "id": "string",
      "location": "string",
      "mapUrl": "https://example.com",
      "name": "Ava Chen",
      "pageUrl": "https://example.com",
      "photoUrl": "https://example.com",
      "priceFrom": 1,
      "prices": [
        {
          "description": "string",
          "earlyBefore": "2026-05-07T12:00:00.000Z",
          "earlyPrice": 1,
          "label": "string",
          "price": 1
        }
      ],
      "priceTo": 1,
      "registrationCloseDate": "2026-05-07T12:00:00.000Z",
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "summary": "string",
      "summaryHtml": "string",
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `created` | date |  |
| `currency` | string |  |
| `displayDate` | string |  |
| `endDate` | date |  |
| `formUrl` | string |  |
| `hideDates` | boolean |  |
| `id` | string |  |
| `location` | string |  |
| `mapUrl` | string |  |
| `name` | string |  |
| `pageUrl` | string |  |
| `photoUrl` | string |  |
| `priceFrom` | number |  |
| `prices[].description` | string |  |
| `prices[].earlyBefore` | date |  |
| `prices[].earlyPrice` | number |  |
| `prices[].label` | string |  |
| `prices[].price` | number |  |
| `priceTo` | number |  |
| `registrationCloseDate` | date |  |
| `startDate` | date |  |
| `status` | string |  |
| `summary` | string |  |
| `summaryHtml` | string |  |
| `timeZone` | string |  |

## Native endpoint

Through the native Corsizio API, this operation is `GET /events` (base URL `https://api.corsizio.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

