# LabsMobile: Schedule SMS

Schedules an SMS message in LabsMobile.

```
POST https://connect.mindcloud.co/v1/universal/labsMobile/latest/actions/schedule-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LabsMobile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/labsMobile/latest/actions/schedule-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "string",
  "recipient[]": [
    {}
  ],
  "scheduled": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/labsMobile/latest/actions/schedule-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": "string",
    "recipient[]": [{}],
    "scheduled": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | string | yes | Scheduled SMS body text. |
| `recipient[]` | array<object> | yes | Recipient array containing msisdn objects. |
| `scheduled` | date | yes | Send time in GMT using YYYY-MM-DD HH:MM:SS. |
| `subid` | string | no | Identifier for the scheduled send. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "message": "string",
      "subid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `message` | string |  |
| `subid` | string |  |

## Native endpoint

Through the native LabsMobile API, this operation is `POST /json/send` (base URL `https://api.labsmobile.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-sms.md) for the provider-specific parameters and requirements.

