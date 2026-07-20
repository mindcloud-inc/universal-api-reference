# Channels: Block MSISDN

Blocks a phone number in Channels.

```
POST https://connect.mindcloud.co/v1/universal/channels/latest/actions/block-msisdn
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/channels/latest/actions/block-msisdn" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "msisdns[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/channels/latest/actions/block-msisdn', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "msisdns[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `msisdns[]` | array<string> | yes | Array of phone numbers to block. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "eventDate": "2026-05-07T12:00:00.000Z",
          "msisdn": "string",
          "status": "string",
          "userId": 1
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
| `[].eventDate` | date |  |
| `[].msisdn` | string |  |
| `[].status` | string |  |
| `[].userId` | number |  |

## Native endpoint

Through the native Channels API, this operation is `POST /api/v1/dnclist/block` (base URL `https://api.channels.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/block-msisdn.md) for the provider-specific parameters and requirements.

