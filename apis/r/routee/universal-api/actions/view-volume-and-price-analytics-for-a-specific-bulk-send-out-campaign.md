# Routee: View Volume and Price Analytics for a specific bulk send out - campaign

Retrieves volume and price analytics for a specific bulk send out - campaign from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/view-volume-and-price-analytics-for-a-specific-bulk-send-out-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/view-volume-and-price-analytics-for-a-specific-bulk-send-out-campaign?connectionId=$CONNECTION_ID&offset=2026-05-07T12%3A00%3A00.000Z&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "offset": "2026-05-07T12:00:00.000Z",
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/view-volume-and-price-analytics-for-a-specific-bulk-send-out-campaign?${params}`, {
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
| `offset` | date | yes | The time offset that the result will be calculated in ISO 8601. |
| `campaignId` | string | yes | The id of the campaign that the messages belong to. |

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
      "smsCampaignId": "string",
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
| `smsCampaignId` | string |  |
| `startDateTime` | string |  |
| `timeGrouping` | string |  |
| `undeliveredCount` | number |  |
| `unsentCount` | number |  |

## Native endpoint

Through the native Routee API, this operation is `GET /reports/my/volPrice/perCampaign` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-volume-and-price-analytics-for-a-specific-bulk-send-out-campaign.md) for the provider-specific parameters and requirements.

