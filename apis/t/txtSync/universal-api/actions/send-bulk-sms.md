# TxtSync: Send Bulk SMS

Creates bulk SMS messages in TxtSync.

```
POST https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/send-bulk-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TxtSync `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/send-bulk-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/send-bulk-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes |  |
| `to` | list<string> | no | Accepts multiple values as an array. |
| `toContactIds` | list<number> | no | Accepts multiple values as an array. |
| `toTagIds` | list<number> | no | Accepts multiple values as an array. |
| `message` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CampaignID": 1,
      "CreatedBy": 1,
      "CreatedDate": "2026-05-07T12:00:00.000Z",
      "CustomerNumber": "string",
      "ModifiedBy": 1,
      "ModifiedDate": "2026-05-07T12:00:00.000Z",
      "Name": "Ava Chen",
      "NumberID": 1,
      "Status": 1,
      "TextMessage": "string",
      "Type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CampaignID` | number |  |
| `CreatedBy` | number |  |
| `CreatedDate` | date |  |
| `CustomerNumber` | string |  |
| `ModifiedBy` | number |  |
| `ModifiedDate` | date |  |
| `Name` | string |  |
| `NumberID` | number |  |
| `Status` | number |  |
| `TextMessage` | string |  |
| `Type` | number |  |

## Native endpoint

Through the native TxtSync API, this operation is `POST /sms/bulk` (base URL `https://api.txtsync.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-bulk-sms.md) for the provider-specific parameters and requirements.

