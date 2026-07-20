# ExpertTexting: Send MMS

Creates an MMS message in ExpertTexting.

```
POST https://connect.mindcloud.co/v1/universal/expertTexting/latest/actions/send-mms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ExpertTexting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/expertTexting/latest/actions/send-mms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string",
  "to": "string",
  "mediaUrls": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/expertTexting/latest/actions/send-mms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string",
    "to": "string",
    "mediaUrls": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes | Paid ExpertTexting MMS-enabled number purchased on your account. |
| `to` | string | yes | Recipient number in international format. |
| `text` | string | no | Optional MMS body text. |
| `mediaUrls` | string | yes | One or more publicly reachable JPG, JPEG, GIF, or PNG URLs for the MMS payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messageCount": 1,
      "messageId": "string",
      "price": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messageCount` | number | Number of MMS message units counted by the provider. |
| `messageId` | string | Provider MMS message ID returned by ExpertTexting. |
| `price` | number | Price returned for the MMS send request. |

## Native endpoint

Through the native ExpertTexting API, this operation is `POST /ExptRestAPI/json/mms/send` (base URL `https://www.experttexting.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-mms.md) for the provider-specific parameters and requirements.

