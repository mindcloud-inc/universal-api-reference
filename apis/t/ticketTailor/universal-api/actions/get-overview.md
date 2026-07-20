# Ticket Tailor: Get Overview

Retrieves box office overview statistics from Ticket Tailor.

```
GET https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/get-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticket Tailor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/get-overview?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/get-overview?${params}`, {
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
      "boxOfficeName": "Ava Chen",
      "currency": {
        "baseMultiplier": 1,
        "code": "string",
        "symbol": "string"
      },
      "eventOccurrencesDraft": 1,
      "eventOccurrencesPublished": 1,
      "eventSeriesDraft": 1,
      "eventSeriesPublished": 1,
      "period": "string",
      "revenue": 1,
      "totalIssuedTickets": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `boxOfficeName` | string |  |
| `currency` | object | Information about revenue currency |
| `currency.baseMultiplier` | number | Base multiplier for conversions |
| `currency.code` | string |  |
| `currency.symbol` | string |  |
| `eventOccurrencesDraft` | number |  |
| `eventOccurrencesPublished` | number |  |
| `eventSeriesDraft` | number |  |
| `eventSeriesPublished` | number |  |
| `period` | string |  |
| `revenue` | number |  |
| `totalIssuedTickets` | number |  |

## Native endpoint

Through the native Ticket Tailor API, this operation is `GET /v1/overview` (base URL `https://api.tickettailor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-overview.md) for the provider-specific parameters and requirements.

