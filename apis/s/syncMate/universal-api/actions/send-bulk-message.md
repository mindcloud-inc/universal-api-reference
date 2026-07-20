# SyncMate: Send Bulk Message



```
POST https://connect.mindcloud.co/v1/universal/syncMate/latest/actions/send-bulk-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SyncMate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/syncMate/latest/actions/send-bulk-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "msgs[]": [
    {}
  ],
  "msgs[].number": "string",
  "msgs[].message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/syncMate/latest/actions/send-bulk-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "msgs[]": [{}],
    "msgs[].number": "string",
    "msgs[].message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `msgs[]` | array<object> | yes |  |
| `msgs[].number` | string | yes | WhatsApp number with country code and no plus sign. |
| `msgs[].message` | string | yes |  |
| `msgs[].media[]` | array<object> | no |  |
| `msgs[].media[].mediaBase64` | string | no | Raw base64 string without the MIME type prefix. |
| `msgs[].media[].fileName` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Bulk send result message from SyncMate. |
| `success` | boolean | Whether SyncMate accepted the bulk message request. |

## Native endpoint

Through the native SyncMate API, this operation is `POST /api/v1/wapushplus/bulk/message` (base URL `https://app.assistro.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-bulk-message.md) for the provider-specific parameters and requirements.

