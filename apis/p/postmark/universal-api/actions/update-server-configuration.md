# Postmark: Update Server Configuration

Updates the current Postmark server configuration.

```
PUT https://connect.mindcloud.co/v1/universal/postmark/latest/actions/update-server-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/update-server-configuration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postmark/latest/actions/update-server-configuration', {
  method: 'PUT',
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

Through the native Postmark API, this operation is `PUT /server` (base URL `https://api.postmarkapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-server-configuration.md) for the provider-specific parameters and requirements.

