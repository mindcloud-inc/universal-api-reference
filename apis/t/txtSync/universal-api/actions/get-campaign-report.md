# TxtSync: Get Campaign Report

Retrieves a campaign report from TxtSync.

```
GET https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/get-campaign-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TxtSync `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/get-campaign-report?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/get-campaign-report?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ActivatedDate": "2026-05-07T12:00:00.000Z",
      "CampaignCost": 1,
      "CurrencyCode": "string",
      "DeliveredCount": 1,
      "FailedCount": 1,
      "FrozenCount": 1,
      "LastSentSMSDate": "2026-05-07T12:00:00.000Z",
      "Links": [
        {}
      ],
      "Name": "Ava Chen",
      "PendingCount": 1,
      "QueuedCount": 1,
      "RecipientCount": 1,
      "SentCount": 1,
      "TotalDistinctOpenedLinks": 1,
      "TotalOpenedLinks": 1,
      "TotalReplies": 1,
      "TrackReplies": true,
      "UndeliveredCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActivatedDate` | date |  |
| `CampaignCost` | number |  |
| `CurrencyCode` | string |  |
| `DeliveredCount` | number |  |
| `FailedCount` | number |  |
| `FrozenCount` | number |  |
| `LastSentSMSDate` | date |  |
| `Links` | array<object> |  |
| `Name` | string |  |
| `PendingCount` | number |  |
| `QueuedCount` | number |  |
| `RecipientCount` | number |  |
| `SentCount` | number |  |
| `TotalDistinctOpenedLinks` | number |  |
| `TotalOpenedLinks` | number |  |
| `TotalReplies` | number |  |
| `TrackReplies` | boolean |  |
| `UndeliveredCount` | number |  |

## Native endpoint

Through the native TxtSync API, this operation is `GET /campaigns/:id/report` (base URL `https://api.txtsync.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-report.md) for the provider-specific parameters and requirements.

