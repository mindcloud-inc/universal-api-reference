# Infobip: Update Scheduled SMS Message Status



```
PUT https://connect.mindcloud.co/v1/universal/infobip/latest/actions/update-scheduled-sms-message-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/update-scheduled-sms-message-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bulkId": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infobip/latest/actions/update-scheduled-sms-message-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bulkId": "string",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bulkId` | string | yes | Unique ID assigned to the request if messaging multiple recipients or sending multiple messages via a single API request. |
| `status` | string | yes | The status of the message(s). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bulkId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bulkId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Infobip API, this operation is `PUT /sms/1/bulks/status` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-scheduled-sms-message-status.md) for the provider-specific parameters and requirements.

