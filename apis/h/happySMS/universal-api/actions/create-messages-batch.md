# Happy SMS: Create Messages Batch



```
POST https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/create-messages-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Happy SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/create-messages-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resources[]": [
    {
      "to": "+687999999",
      "message": "MindCloud bulk test",
      "priority": "LOW"
    }
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/create-messages-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resources[]": [{"to":"+687999999","message":"MindCloud bulk test","priority":"LOW"}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resources[]` | array<object> | yes | Array of SMS message resources to create in bulk. Default: `[{"to":"+687999999","message":"MindCloud bulk test","priority":"LOW"}]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "anonymized": true,
          "externalId": "string",
          "from": "string",
          "id": 1,
          "lastStatus": "string",
          "lastStatusDate": "string",
          "message": "string",
          "priority": "string",
          "sender": "string",
          "smsCreditUsed": 1,
          "statusMessage": "string",
          "timeToLive": "string",
          "to": "string"
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
| `[].anonymized` | boolean | Whether the SMS has been anonymized. |
| `[].externalId` | string | Caller-defined external identifier. |
| `[].from` | string | Sender phone number. |
| `[].id` | number | Unique SMS identifier. |
| `[].lastStatus` | string | Latest message status. |
| `[].lastStatusDate` | string | Timestamp of the latest status change. |
| `[].message` | string | SMS body content. |
| `[].priority` | string | SMS priority. |
| `[].sender` | string | Origin channel of the SMS. |
| `[].smsCreditUsed` | number | SMS credits consumed. |
| `[].statusMessage` | string | Status detail when an error occurs. |
| `[].timeToLive` | string | Expiration timestamp for the SMS. |
| `[].to` | string | Recipient phone number. |

## Native endpoint

Through the native Happy SMS API, this operation is `POST /api/v1/protected/domain/sms/bulk/messages` (base URL `https://www.api.nc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-messages-batch.md) for the provider-specific parameters and requirements.

