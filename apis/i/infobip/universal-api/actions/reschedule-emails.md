# Infobip: Reschedule Emails



```
PUT https://connect.mindcloud.co/v1/universal/infobip/latest/actions/reschedule-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/reschedule-emails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bulkId": "string",
  "sendAt": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infobip/latest/actions/reschedule-emails', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bulkId": "string",
    "sendAt": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bulkId` | string | yes | The ID that uniquely identifies the sent bulk. |
| `sendAt` | date | yes | Date and time when the email is to be sent. Has the following format: `yyyy-MM-dd'T'HH:mm:ss.SSSZ`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bulkId": "string",
      "sendAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bulkId` | string |  |
| `sendAt` | date |  |

## Native endpoint

Through the native Infobip API, this operation is `PUT /email/1/bulks` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reschedule-emails.md) for the provider-specific parameters and requirements.

