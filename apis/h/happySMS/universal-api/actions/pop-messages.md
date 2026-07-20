# Happy SMS: Pop Messages



```
GET https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/pop-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Happy SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/pop-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/pop-messages?${params}`, {
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
| `limit` | number | no | Maximum number of recently modified messages to pop. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
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
          "to": "string"
        }
      ],
      "listInfoMessages": [
        [
          "string"
        ]
      ],
      "listWarningMessages": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Total number of matching messages returned by the pop call. |
| `data[].anonymized` | boolean | Whether the SMS has been anonymized. |
| `data[].externalId` | string | Caller-defined external identifier. |
| `data[].from` | string | Sender phone number. |
| `data[].id` | number | Unique SMS identifier. |
| `data[].lastStatus` | string | Latest message status. |
| `data[].lastStatusDate` | string | Timestamp of the latest status change. |
| `data[].message` | string | SMS body content. |
| `data[].priority` | string | SMS priority. |
| `data[].sender` | string | Origin channel of the SMS. |
| `data[].smsCreditUsed` | number | SMS credits consumed. |
| `data[].statusMessage` | string | Status detail when an error occurs. |
| `data[].to` | string | Recipient phone number. |
| `listInfoMessages[]` | array<string> | Informational messages returned by the API. |
| `listWarningMessages[]` | array<string> | Warning messages returned by the API. |

## Native endpoint

Through the native Happy SMS API, this operation is `GET /api/v1/protected/domain/sms/messages/pop` (base URL `https://www.api.nc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pop-messages.md) for the provider-specific parameters and requirements.

