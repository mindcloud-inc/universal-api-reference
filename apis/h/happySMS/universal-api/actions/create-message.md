# Happy SMS: Create Message



```
POST https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/create-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Happy SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/create-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": "+687999999",
  "priority": "LOW",
  "message": "MindCloud validator test"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/create-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": "+687999999",
    "priority": "LOW",
    "message": "MindCloud validator test"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `to` | string | yes | Recipient phone number in +687XXXXXX format. Default: `+687999999`. |
| `from` | string | no | Sender phone number. Optional when the API key already defines the sender. |
| `priority` | string | yes | SMS priority: LOW or HIGH. Default: `LOW`. |
| `message` | string | yes | SMS body content. Default: `MindCloud validator test`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timeToLive` | string | no | ISO 8601 expiration timestamp for the SMS. |
| `externalId` | string | no | Optional caller-defined identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "anonymized": true,
      "externalId": "string",
      "from": "string",
      "historiesStatus": [
        {
          "message": "string",
          "status": "string",
          "statusDate": "string"
        }
      ],
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `anonymized` | boolean | Whether the SMS has been anonymized. |
| `externalId` | string | Caller-defined external identifier. |
| `from` | string | Sender phone number. |
| `historiesStatus[].message` | string | Status history detail message. |
| `historiesStatus[].status` | string | Status history entry status. |
| `historiesStatus[].statusDate` | string | Status history timestamp. |
| `id` | number | Unique SMS identifier. |
| `lastStatus` | string | Latest message status. |
| `lastStatusDate` | string | Timestamp of the latest status change. |
| `message` | string | SMS body content. |
| `priority` | string | SMS priority. |
| `sender` | string | Origin channel of the SMS. |
| `smsCreditUsed` | number | SMS credits consumed. |
| `statusMessage` | string | Status detail when an error occurs. |
| `timeToLive` | string | Expiration timestamp for the SMS. |
| `to` | string | Recipient phone number. |

## Native endpoint

Through the native Happy SMS API, this operation is `POST /api/v1/protected/domain/sms/messages` (base URL `https://www.api.nc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-message.md) for the provider-specific parameters and requirements.

