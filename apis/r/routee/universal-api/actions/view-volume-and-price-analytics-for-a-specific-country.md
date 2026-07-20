# Routee: View Volume and Price Analytics for a specific country

Retrieves volume and price analytics for a specific country from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/view-volume-and-price-analytics-for-a-specific-country
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/view-volume-and-price-analytics-for-a-specific-country?connectionId=$CONNECTION_ID&startDate=string&endDate=string&mcc=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "string",
  "endDate": "string",
  "mcc": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/view-volume-and-price-analytics-for-a-specific-country?${params}`, {
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
| `startDate` | string | yes | starting date to get reports |
| `endDate` | string | yes | ending date to get reports |
| `mcc` | string | yes | the mcc code |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "country": "string",
      "deliveredCount": 1,
      "failedCount": 1,
      "mcc": "string",
      "mnc": "string",
      "operator": "string",
      "price": 1,
      "queuedCount": 1,
      "sentCount": 1,
      "startDateTime": "string",
      "timeGrouping": "string",
      "undeliveredCount": 1,
      "unsentCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `country` | string |  |
| `deliveredCount` | number |  |
| `failedCount` | number |  |
| `mcc` | string |  |
| `mnc` | string |  |
| `operator` | string |  |
| `price` | number |  |
| `queuedCount` | number |  |
| `sentCount` | number |  |
| `startDateTime` | string |  |
| `timeGrouping` | string |  |
| `undeliveredCount` | number |  |
| `unsentCount` | number |  |

## Native endpoint

Through the native Routee API, this operation is `GET /reports/my/volPrice/perMcc` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-volume-and-price-analytics-for-a-specific-country.md) for the provider-specific parameters and requirements.

