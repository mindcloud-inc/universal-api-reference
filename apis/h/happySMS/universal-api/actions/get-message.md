# Happy SMS: Get Message



```
GET https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Happy SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/get-message?connectionId=$CONNECTION_ID&id=999999999" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "999999999"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/get-message?${params}`, {
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
| `id` | number | yes | Unique SMS identifier. Default: `999999999`. |

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

Through the native Happy SMS API, this operation is `GET /api/v1/protected/domain/sms/messages/:id` (base URL `https://www.api.nc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.

