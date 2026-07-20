# TxtSync: List SMS

Retrieves SMS messages from TxtSync.

```
GET https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/list-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TxtSync `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/list-sms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/list-sms?${params}`, {
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
      "ApplicationID": 1,
      "ApplicationName": "Ava Chen",
      "CampaignID": 1,
      "ContactID": 1,
      "ContactName": "Ava Chen",
      "CostGBP": 1,
      "CostLocal": 1,
      "CreatedDate": "2026-05-07T12:00:00.000Z",
      "CurrencyCode": "string",
      "DeliveredDate": "2026-05-07T12:00:00.000Z",
      "Direction": 1,
      "ErrorCode": "string",
      "FlaggedDate": "2026-05-07T12:00:00.000Z",
      "FlaggedDescription": "string",
      "FromNumber": "string",
      "IsFlagged": true,
      "LinkDetails": "https://example.com",
      "Message": "string",
      "ProfileURL": "https://example.com",
      "Segments": 1,
      "SMSID": 1,
      "Status": 1,
      "ToNumber": "string",
      "UserID": 1,
      "UserName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ApplicationID` | number |  |
| `ApplicationName` | string |  |
| `CampaignID` | number |  |
| `ContactID` | number |  |
| `ContactName` | string |  |
| `CostGBP` | number |  |
| `CostLocal` | number |  |
| `CreatedDate` | date |  |
| `CurrencyCode` | string |  |
| `DeliveredDate` | date |  |
| `Direction` | number |  |
| `ErrorCode` | string |  |
| `FlaggedDate` | date |  |
| `FlaggedDescription` | string |  |
| `FromNumber` | string |  |
| `IsFlagged` | boolean |  |
| `LinkDetails` | string |  |
| `Message` | string |  |
| `ProfileURL` | string |  |
| `Segments` | number |  |
| `SMSID` | number |  |
| `Status` | number |  |
| `ToNumber` | string |  |
| `UserID` | number |  |
| `UserName` | string |  |

## Native endpoint

Through the native TxtSync API, this operation is `GET /sms` (base URL `https://api.txtsync.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sms.md) for the provider-specific parameters and requirements.

