# Sponsy: List Publications

Retrieves publications from Sponsy.

```
GET https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-publications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sponsy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-publications?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-publications?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "days": [
        "string"
      ],
      "hideBlockedDates": true,
      "id": "string",
      "name": "Ava Chen",
      "order": 1,
      "scheduleFrequency": "string",
      "scheduleFrequencyValue": 1,
      "scheduleReferenceTo": "string",
      "slug": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedAt` | date | Archive timestamp when present. |
| `createdAt` | date | Publication creation timestamp. |
| `days` | array<string> | Scheduled publication weekdays. |
| `hideBlockedDates` | boolean | Whether blocked dates are hidden in the calendar. |
| `id` | string | Sponsy publication ID. |
| `name` | string | Publication name. |
| `order` | number | Publication display order. |
| `scheduleFrequency` | string | Publication schedule cadence. |
| `scheduleFrequencyValue` | number | Schedule cadence interval value. |
| `scheduleReferenceTo` | string | Publication schedule reference type. |
| `slug` | string | Publication slug. |
| `type` | string | Publication type. |
| `updatedAt` | date | Publication update timestamp. |

## Native endpoint

Through the native Sponsy API, this operation is `GET /v1/publications` (base URL `https://api.getsponsy.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-publications.md) for the provider-specific parameters and requirements.

