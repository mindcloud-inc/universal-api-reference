# TxtSync: Get Campaign

Retrieves a specific campaign from TxtSync.

```
GET https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TxtSync `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/get-campaign?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/get-campaign?${params}`, {
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
      "CampaignID": 1,
      "CostGBP": 1,
      "CostLocal": 1,
      "CreatedBy": 1,
      "CreatedByApp": 1,
      "CreatedByAppName": "Ava Chen",
      "CreatedByName": "Ava Chen",
      "CreatedDate": "2026-05-07T12:00:00.000Z",
      "CurrencyCode": "string",
      "CustomerNumber": "string",
      "IncludeWebOptOut": true,
      "IsSharedNumber": true,
      "LastSentSMSDate": "2026-05-07T12:00:00.000Z",
      "ModifiedBy": 1,
      "ModifiedByApp": 1,
      "ModifiedByAppName": "Ava Chen",
      "ModifiedByName": "Ava Chen",
      "ModifiedDate": "2026-05-07T12:00:00.000Z",
      "Name": "Ava Chen",
      "NumberID": 1,
      "ProcessedContacts": 1,
      "ScheduledDate": "2026-05-07T12:00:00.000Z",
      "Status": 1,
      "TextMessage": "string",
      "TotalContacts": 1,
      "TotalDistinctOpenedLinks": 1,
      "TotalOpenedLinks": 1,
      "TotalReplies": 1,
      "TrackReplies": true,
      "Type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActivatedDate` | date |  |
| `CampaignID` | number |  |
| `CostGBP` | number |  |
| `CostLocal` | number |  |
| `CreatedBy` | number |  |
| `CreatedByApp` | number |  |
| `CreatedByAppName` | string |  |
| `CreatedByName` | string |  |
| `CreatedDate` | date |  |
| `CurrencyCode` | string |  |
| `CustomerNumber` | string |  |
| `IncludeWebOptOut` | boolean |  |
| `IsSharedNumber` | boolean |  |
| `LastSentSMSDate` | date |  |
| `ModifiedBy` | number |  |
| `ModifiedByApp` | number |  |
| `ModifiedByAppName` | string |  |
| `ModifiedByName` | string |  |
| `ModifiedDate` | date |  |
| `Name` | string |  |
| `NumberID` | number |  |
| `ProcessedContacts` | number |  |
| `ScheduledDate` | date |  |
| `Status` | number |  |
| `TextMessage` | string |  |
| `TotalContacts` | number |  |
| `TotalDistinctOpenedLinks` | number |  |
| `TotalOpenedLinks` | number |  |
| `TotalReplies` | number |  |
| `TrackReplies` | boolean |  |
| `Type` | number |  |

## Native endpoint

Through the native TxtSync API, this operation is `GET /campaigns/:id` (base URL `https://api.txtsync.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

