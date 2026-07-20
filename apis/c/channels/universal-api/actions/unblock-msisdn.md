# Channels: Unblock MSISDN

Unblocks a phone number in Channels.

```
DELETE https://connect.mindcloud.co/v1/universal/channels/latest/actions/unblock-msisdn
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/channels/latest/actions/unblock-msisdn?connectionId=$CONNECTION_ID&msisdns%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "msisdns[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channels/latest/actions/unblock-msisdn?${params}`, {
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
| `msisdns[]` | array<string> | yes | Array of phone numbers to unblock. Accepts multiple values as an array. |

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

Through the native Channels API, this operation is `POST /api/v1/dnclist/unblock` (base URL `https://api.channels.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unblock-msisdn.md) for the provider-specific parameters and requirements.

