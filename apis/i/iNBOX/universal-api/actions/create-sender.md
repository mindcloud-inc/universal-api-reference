# INBOX: Create Sender

Creates a new sender in INBOX.

```
POST https://connect.mindcloud.co/v1/universal/iNBOX/latest/actions/create-sender
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a INBOX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iNBOX/latest/actions/create-sender" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iNBOX/latest/actions/create-sender', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "resultCode": 1,
      "resultMessage": "string",
      "resultObject": {},
      "resultStatus": true,
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resultCode` | number |  |
| `resultMessage` | string |  |
| `resultObject` | object |  |
| `resultStatus` | boolean |  |
| `version` | string |  |

## Native endpoint

Through the native INBOX API, this operation is `POST /inbox/v1/senders` (base URL `https://useapi.useinbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sender.md) for the provider-specific parameters and requirements.

