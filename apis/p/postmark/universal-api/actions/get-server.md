# Postmark: Get Server

Retrieves a server from Postmark.

```
GET https://connect.mindcloud.co/v1/universal/postmark/latest/actions/get-server
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/get-server?connectionId=$CONNECTION_ID&serverId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "serverId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmark/latest/actions/get-server?${params}`, {
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
| `serverId` | string | yes | The Postmark server ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Color": "string",
      "DeliveryType": "string",
      "ID": 1,
      "InboundAddress": "string",
      "Name": "Ava Chen",
      "ServerLink": "https://example.com",
      "TrackLinks": "https://example.com",
      "TrackOpens": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Color` | string |  |
| `DeliveryType` | string |  |
| `ID` | number |  |
| `InboundAddress` | string |  |
| `Name` | string |  |
| `ServerLink` | string |  |
| `TrackLinks` | string |  |
| `TrackOpens` | boolean |  |

## Native endpoint

Through the native Postmark API, this operation is `GET /servers/:serverId` (base URL `https://api.postmarkapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-server.md) for the provider-specific parameters and requirements.

