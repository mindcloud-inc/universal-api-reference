# Moosend: Get Campaign Summary

Retrieves campaign summary from Moosend.

```
GET https://connect.mindcloud.co/v1/universal/moosend/latest/actions/get-campaign-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/get-campaign-summary?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moosend/latest/actions/get-campaign-summary?${params}`, {
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
| `campaignId` | string | yes | The ID of the campaign that you want to get a summary of. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abVersion": "string",
      "campaignDeliveredOn": "2026-05-07T12:00:00.000Z",
      "campaignID": "string",
      "campaignIsArchived": true,
      "campaignName": "Ava Chen",
      "campaignSubject": "string",
      "from": "2026-05-07T12:00:00.000Z",
      "mailingLists": [
        {}
      ],
      "sent": 1,
      "to": "2026-05-07T12:00:00.000Z",
      "totalBounces": 1,
      "totalComplaints": 1,
      "totalForwards": 1,
      "totalLinkClicks": 1,
      "totalOpens": 1,
      "totalUnsubscribes": 1,
      "uniqueForwards": 1,
      "uniqueLinkClicks": 1,
      "uniqueOpens": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abVersion` | string |  |
| `campaignDeliveredOn` | date |  |
| `campaignID` | string |  |
| `campaignIsArchived` | boolean |  |
| `campaignName` | string |  |
| `campaignSubject` | string |  |
| `from` | date |  |
| `mailingLists` | array<object> |  |
| `sent` | number |  |
| `to` | date |  |
| `totalBounces` | number |  |
| `totalComplaints` | number |  |
| `totalForwards` | number |  |
| `totalLinkClicks` | number |  |
| `totalOpens` | number |  |
| `totalUnsubscribes` | number |  |
| `uniqueForwards` | number |  |
| `uniqueLinkClicks` | number |  |
| `uniqueOpens` | number |  |

## Native endpoint

Through the native Moosend API, this operation is `GET /campaigns/{{CampaignID}}/view-summary.json` (base URL `https://api.moosend.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-summary.md) for the provider-specific parameters and requirements.

