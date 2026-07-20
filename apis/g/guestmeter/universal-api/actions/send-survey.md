# Guestmeter: Send Survey

Creates a guest survey request in Guestmeter.

```
POST https://connect.mindcloud.co/v1/universal/guestmeter/latest/actions/send-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Guestmeter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/guestmeter/latest/actions/send-survey" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "guestEmail": "guest@example.com",
  "guestName": "Jane Guest"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/guestmeter/latest/actions/send-survey', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "guestEmail": "guest@example.com",
    "guestName": "Jane Guest"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checkoutDate` | string | no | Optional send date in DD.MM.YYYY or DD-MM-YYYY format. Example: `31.12.2026`. |
| `guestEmail` | string | yes | Guest email address. Example: `guest@example.com`. |
| `guestName` | string | yes | Guest full name. Example: `Jane Guest`. |
| `guestPhone` | string | no | Guest mobile number in international format. Example: `+15551234567`. |
| `integrationID` | string | no | Reference ID for the guest in your source system (for example reservation ID). Example: `reservation-12345`. |
| `languageCode` | string | no | Two-letter language code (for example en). Default: `en`. Example: `en`. |
| `primarySendMethod` | string | no | Preferred channel when both email and phone exist: email or sms. Example: `email`. |
| `roomNumber` | string | no | Guest room number or table number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "statusList": [
        {
          "status": "string",
          "statusCode": "string",
          "statusMessage": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `statusList` | array<object> |  |
| `statusList[].status` | string |  |
| `statusList[].statusCode` | string |  |
| `statusList[].statusMessage` | string |  |

## Native endpoint

Through the native Guestmeter API, this operation is `POST /sendSurvey` (base URL `https://www.guestmeter.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-survey.md) for the provider-specific parameters and requirements.

