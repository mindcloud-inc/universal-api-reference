# Eventzilla: List Events

Retrieves events from Eventzilla.

```
GET https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventzilla `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/list-events?${params}`, {
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
| `status` | string | no | Filter events by Eventzilla status such as live or completed. |
| `category` | string | no | Filter events by category. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bgimageUrl": "https://example.com",
      "categories": "string",
      "currency": "string",
      "dateid": 1,
      "description": "string",
      "descriptionHtml": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "endTime": "string",
      "id": 1,
      "inviteCode": "string",
      "language": "string",
      "logoUrl": "https://example.com",
      "showRemaining": true,
      "startDate": "2026-05-07T12:00:00.000Z",
      "startTime": "string",
      "status": "string",
      "ticketsSold": 1,
      "ticketsTotal": 1,
      "timeZone": "string",
      "timezoneCode": "string",
      "title": "string",
      "twitterHashtag": "string",
      "url": "https://example.com",
      "utcOffset": "string",
      "venue": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bgimageUrl` | string |  |
| `categories` | string |  |
| `currency` | string |  |
| `dateid` | number |  |
| `description` | string |  |
| `descriptionHtml` | string |  |
| `endDate` | date |  |
| `endTime` | string |  |
| `id` | number |  |
| `inviteCode` | string |  |
| `language` | string |  |
| `logoUrl` | string |  |
| `showRemaining` | boolean |  |
| `startDate` | date |  |
| `startTime` | string |  |
| `status` | string |  |
| `ticketsSold` | number |  |
| `ticketsTotal` | number |  |
| `timeZone` | string |  |
| `timezoneCode` | string |  |
| `title` | string |  |
| `twitterHashtag` | string |  |
| `url` | string |  |
| `utcOffset` | string |  |
| `venue` | string |  |

## Native endpoint

Through the native Eventzilla API, this operation is `GET /events` (base URL `https://www.eventzillaapi.net/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

