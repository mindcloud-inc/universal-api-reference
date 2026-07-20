# TxtSync: Send Single SMS

Creates a single SMS message in TxtSync.

```
POST https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/send-single-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TxtSync `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/send-single-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/send-single-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | no |  |
| `to` | string | no |  |
| `toContactId` | number | no |  |
| `message` | string | yes |  |

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

Through the native TxtSync API, this operation is `POST /sms/send` (base URL `https://api.txtsync.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-single-sms.md) for the provider-specific parameters and requirements.

