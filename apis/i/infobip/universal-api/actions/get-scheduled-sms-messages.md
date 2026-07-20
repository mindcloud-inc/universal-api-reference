# Infobip: Get Scheduled SMS Messages



```
GET https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-scheduled-sms-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-scheduled-sms-messages?connectionId=$CONNECTION_ID&bulkId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bulkId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-scheduled-sms-messages?${params}`, {
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
| `bulkId` | string | yes | Unique ID assigned to the request if messaging multiple recipients or sending multiple messages via a single API request. |

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

Through the native Infobip API, this operation is `GET /sms/1/bulks` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scheduled-sms-messages.md) for the provider-specific parameters and requirements.

